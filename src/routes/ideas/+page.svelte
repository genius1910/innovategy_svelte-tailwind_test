<script>
	import { goto } from '$app/navigation';
	import largePlus from '$lib/images/large-plus.svg';
</script>

<div class="pt-12 flex flex-col sm:pl-[87px] px-7 gap-14">
	<div class="flex flex-col gap-3">
		<p class=" text-[40px] text-[#001638] leading-14 font-semibold">Ideas & Projects</p>
		<span class="text-4 leading-6 font-medium text-[#252525]">
			Add your ideas and projects here.
		</span>
	</div>
	<div class="flex sm:flex-row flex-col gap-4">
		<div class="px-4 pt-1 pb-2 bg-[#FAFAFA] rounded-lg gap-[2px]">
			<div class="w-max px-1 bg-[#FFF2E4] rounded-md">
				<p class="text-[#FF921B] text-[14px] leading-6 font-normal">Idea</p>
			</div>
			<p class="text-[#001638] text-4 leading-6 font-medium">Food Delivery App</p>
		</div>
		<div class="px-4 pt-1 pb-2 bg-[#FAFAFA] rounded-lg gap-[2px]">
			<div class="w-max px-1 bg-[#EBFAE2] rounded-md">
				<p class="text-[#68C132] text-[14px] leading-6 font-normal">Project</p>
			</div>
			<p class="text-[#001638] text-4 leading-6 font-medium">Accountant Product</p>
		</div>
		<button
			on:click={() => goto('/ideas/create')}
			class="flex p-[19px] bg-[#FAFAFA] rounded-lg gap-[2px] items-center justify-center"
		>
			<img src={largePlus} alt="SvelteKit" />
		</button>
	</div>
</div>
