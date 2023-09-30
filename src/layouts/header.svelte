<script>
	import logo from '$lib/images/logo.svg';
	import helpCircle from '$lib/images/help-circle.svg';
	import user from '$lib/images/user-log.svg';
	import Navbar from './navbar.svelte';
	let menuState = false;
	let navState = false;
</script>

<svelte:head>
	<link rel="stylesheet" href="https://unpkg.com/mono-icons@1.2.1/iconfont/icons.css" />
</svelte:head>

<div
	class="fixed w-screen h-[115px] flex flex-row justify-between px-7 items-center border shadow bg-white gap-4"
>
	<div
		class="text-[#000] text-2xl block md:hidden"
		role="button"
		tabindex=""
		on:click={() => (navState = !navState)}
		on:keydown={(e) => {
			if (e.key === 'Enter') navState = !navState;
		}}
	>
		{#if navState}
			<i class="mi mi-close" />
		{:else}
			<i class="mi mi-menu" />
		{/if}
	</div>
	<div
		class={`absolute top-32 left-3 ${
			navState ? 'block' : 'hidden'
		} bg-white rounded-lg pb-4 border-4 border-zinc-800`}
		role="button"
		tabindex=""
		on:click={() => (navState = !navState)}
		on:keydown={(e) => {
			if (e.key === 'Enter') navState = !navState;
		}}
	>
		<Navbar />
	</div>
	<a href="/">
		<img src={logo} alt="SvelteKit" />
	</a>
	<div
		class="text-[#000] text-2xl block md:hidden"
		role="button"
		tabindex=""
		on:click={() => (menuState = !menuState)}
		on:keydown={(e) => {
			if (e.key === 'Enter') menuState = !menuState;
		}}
	>
		{#if menuState}
			<i class="mi mi-close" />
		{:else}
			<i class="mi mi-menu" />
		{/if}
	</div>
	<div class="md:flex flex-row justify-center items-center gap-8 hidden">
		<div class="flex flex-row justify-center items-center gap-2 cursor-pointer">
			<img src={helpCircle} alt="SvelteKit" />
			<p class="normal-font">Need Help?</p>
		</div>
		<a href="/signin" class="flex flex-row justify-center items-center gap-2 cursor-pointer">
			<img src={user} alt="SvelteKit" />
			<p class="normal-font hover:outline-none">Sign Up</p>
		</a>
	</div>
	<div
		class={`absolute top-32 right-3 ${
			menuState ? 'block' : 'hidden'
		} bg-white rounded-lg p-4 border-4 border-zinc-800 flex flex-col gap-4`}
		role="button"
		tabindex=""
		on:click={() => (menuState = !menuState)}
		on:keydown={(e) => {
			if (e.key === 'Enter') menuState = !menuState;
		}}
	>
		<div class="flex flex-row justify-start items-center gap-2 cursor-pointer">
			<img src={helpCircle} alt="SvelteKit" />
			<p class="normal-font">Need Help?</p>
		</div>
		<a href="/signin" class="flex flex-row justify-start items-center gap-2 cursor-pointer">
			<img src={user} alt="SvelteKit" />
			<p class="normal-font hover:outline-none">Sign Up</p>
		</a>
	</div>
</div>
