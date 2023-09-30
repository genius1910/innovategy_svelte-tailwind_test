<script>
	import plus from '$lib/images/plus.svg';
</script>

<div class="pt-12 flex flex-col sm:pl-[87px] px-7 gap-8 max-w-[670px] w-full">
	<div class="flex flex-col gap-3 w-full">
		<p class=" text-[40px] text-[#001638] leading-14 font-semibold">Add Clients</p>
		<span class="text-4 leading-6 font-medium text-[#252525] w-full">
			Currently, you don’t have any clients added here. To add clients click to the “Add Clients” button.
		</span>
	</div>
	<div class="flex flex-row justify-end max-w-[544px] gap-4">
		<button
			class="py-2 px-4 border rounded-lg text-center shadow-[0_3px_1px_-2px_#0000000F] border-[#CACFD5] text-[14px] leading-6 font-medium text-[#2B3E59]"
		>
			Back
		</button>
		<button
			class="flex flex-row justify-center items-center gap-2 py-2 px-4 border rounded-lg text-center shadow-[0_3px_1px_-2px_#0000000F] border-[#CACFD5] text-[14px] leading-6 font-medium text-[#FFFFFF] bg-[#0CBFAD]"
		>
			<p>Add Clients</p>
			<img src={plus} alt="SvelteKit" />
		</button>
	</div>
</div>
