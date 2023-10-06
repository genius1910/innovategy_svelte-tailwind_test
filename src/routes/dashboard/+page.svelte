<script>
	import { writable } from 'svelte/store';

	let select = writable('');

	function setSelect(value) {
		$select = value;
	}
</script>

<div class="pt-12 flex flex-col sm:pl-[87px] pl-7 pr-7 gap-14">
	<div class="flex flex-col gap-3">
		<p class=" text-[40px] text-[#001638] leading-14 font-semibold">Welcome!</p>
		<p class="text-4 leading-6 font-medium text-[#252525]">
			Please tell us a bit so we can enhance your experience:
		</p>
	</div>
	<div class="flex flex-col gap-8 w-full sm:w-max">
		<div class="flex flex-col xl:flex-row gap-4 w-full">
			<div
				role="button"
				tabindex=""
				class={`w-full sm:w-[369px] py-4 gap-[2px] border border-[#DEDEDE] hover:bg-[#dcfdfa] duration-500 rounded-lg text-center shadow-[0_3px_1px_-2px_#0000000F] ${
					$select == 'clients' ? 'bg-[#CFFBF7]' : 'bg-white'
				}`}
				on:click={() => setSelect('clients')}
				on:keydown={(e) => {
					if (e.key === 'Enter') setSelect('clients');
				}}
			>
				<p class="text-4 leading-6 font-medium text-[#001638]">
					I want to manage my clients projects
				</p>
				<p class="text-[14px] leading-6 font-normal text-[#333333]">
					Agencies, freelancers and consultants
				</p>
			</div>
			<div
				role="button"
				tabindex=""
				class={`w-full sm:w-[369px] py-4 gap-[2px] border border-[#DEDEDE] hover:bg-[#dcfdfa] duration-500 rounded-lg text-center shadow-[0_3px_1px_-2px_#0000000F] ${
					$select == 'business' ? 'bg-[#CFFBF7]' : 'bg-white'
				}`}
				on:click={() => setSelect('business')}
				on:keydown={(e) => {
					if (e.key === 'Enter') setSelect('business');
				}}
			>
				<p class="text-4 leading-6 font-medium text-[#001638]">
					I want to manage my own business’s projects
				</p>
				<p class="text-[14px] leading-6 font-normal text-[#333333]">
					Startups, SME Businesses, non-profit organizations
				</p>
			</div>
		</div>
		<div class="flex flex-row xl:justify-end justify-center gap-4 w-full">
			<button class="normal-active-button text-[#2B3E59] bg-white hover:bg-slate-100"> Cancle </button>
			<button
				class={`normal-active-button ${
					!$select
						? 'text-[#A4ABB8] bg-[#F5F5F6] cursor-not-allowed'
						: 'bg-[#0CBFAD] hover:bg-[#0AB0A0] text-white'
				}`}
				disabled={$select ? false : true}
			>
				Next
			</button>
		</div>
	</div>
</div>
