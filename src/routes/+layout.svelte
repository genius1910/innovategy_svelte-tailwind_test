<script>
	import './styles.css';
	import { page } from '$app/stores';
	import Footer from '../layouts/footer.svelte';
	import Header from '../layouts/header.svelte';
	import Navbar from '../layouts/navbar.svelte';
	let route;
	$: route = $page.url.pathname;
</script>

<div class="app flex min-w-full min-h-full flex-col h-screen bg-white">
	{#if route == '/' || route == '/signin' || route == '/signup'}
		<slot />
	{:else}
		<div class="flex-none">
			<Header />
		</div>
		<div class="flex w-full flex-1 pt-[115px] h-96">
			{#if route != '/ideas/create'}
				<div class="flex-none border-r hidden md:block">
					<Navbar />
				</div>
			{/if}
			<div class="flex-1 overflow-auto">
				<slot />
			</div>
		</div>
		{#if route != '/ideas/create'}
			<div class="flex-none">
				<Footer />
			</div>
		{/if}
	{/if}
</div>

<style>
</style>
