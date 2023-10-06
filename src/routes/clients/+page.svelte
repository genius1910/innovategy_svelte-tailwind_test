<script>
	import plus from '$lib/images/plus.svg';
</script>

<div class="pt-12 flex flex-col sm:pl-[87px] px-7 gap-8 max-w-[670px] w-full">
	<div class="flex flex-col gap-3 w-full">
		<p class=" text-[40px] text-[#001638] leading-14 font-semibold">Add Clients</p>
		<span class="text-4 leading-6 font-medium text-[#252525] w-full">
			Currently, you don’t have any clients added here. To add clients click to the “Add Clients”
			button.
		</span>
	</div>
	<div class="flex flex-row justify-end max-w-[544px] gap-4">
		<button class="normal-active-button text-[#2B3E59] bg-white hover:bg-slate-100"> Back </button>
		<button
			class="flex flex-row justify-center items-center gap-2 normal-active-button text-[#FFFFFF] bg-[#0CBFAD] hover:bg-[#0AB0A0]"
		>
			<p>Add Clients</p>
			<img src={plus} alt="SvelteKit" />
		</button>
	</div>
</div>
