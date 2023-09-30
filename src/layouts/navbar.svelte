<script>
	import { page } from '$app/stores';
	import { goto } from '$app/navigation';
	const menus = [
		{
			img: 'icon-dashboard',
			title: 'Dashboard',
			url: '/dashboard',
			key: 'dashboard'
		},
		{
			img: 'smile',
			title: 'Clients',
			url: '/clients',
			key: 'clients'
		},
		{
			img: 'codesandbox',
			title: 'Ideas',
			url: '/ideas',
			key: 'ideas'
		},
		{
			img: 'database',
			title: 'Projects',
			url: '/projects',
			key: 'projects'
		},
		{
			img: 'settings',
			title: 'Settings',
			url: '/settings',
			key: 'settings'
		},
		{
			img: 'users',
			title: 'Team Members',
			url: '/team',
			key: 'team'
		},
		{
			img: 'lock',
			title: 'Plan & Subscription',
			url: '/plan',
			key: 'plan'
		},
		{
			img: 'send',
			title: 'Support',
			url: '/support',
			key: 'support'
		}
	];
	console.log($page.url.pathname);
</script>

<div class="w-64 h-full flex flex-col pt-8 px-4">
	{#each menus as menu, index (index)}
		<!-- svelte-ignore a11y-click-events-have-key-events -->
		<div
			role="button"
			tabindex={index}
			on:click={() => goto(menu.url)}
			class={`flex flex-row justify-start gap-3 normal-font pl-3 cursor-pointer hover:bg-[#F6F6F6] transition duration-500 ${
				$page.url.pathname.includes(menu.key) ? 'bg-[#F6F6F6]' : ''
			}`}
		>
			<img src={'/src/lib/images/' + menu.img + '.svg'} alt="SvelteKit" />
			<p class="p-2">{menu.title}</p>
		</div>
	{/each}
</div>
