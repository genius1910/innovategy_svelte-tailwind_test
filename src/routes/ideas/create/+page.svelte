<script>
	let value = '';
</script>

<div class="pt-12 flex flex-col xl:px-[150px] px-10 gap-3">
	<p class=" text-[40px] text-[#001638] leading-14 font-semibold">Ideas</p>
	<div class="flex lg:flex-row flex-col gap-[100px] justify-start">
		<div class="flex flex-1 flex-col gap-8">
			<span class="text-4 leading-6 font-medium text-[#252525]">
				Please tell us a bit about your project/idea so we can enhance your experience:
			</span>
			<textarea
				class="w-full h-[176px] border border-[#CACFD5] rounded-lg pt-2 pl-4 text-[#7D8899] text-[14px] leading-6 font-normal focus:outline-slate-700"
				placeholder="Start typing your idea here"
				bind:value
			/>
			<div class="flex flex-row justify-end gap-4">
				<button
					class={`normal-active-button ${
						!value
							? 'text-[#A4ABB8] bg-[#F5F5F6] cursor-not-allowed'
							: 'bg-[#0CBFAD] hover:bg-[#0AB0A0] text-white'
					}`}
					disabled={value ? false : true}
				>
					What Do You Think?
				</button>
			</div>
		</div>
		<div class="xl:w-[446px] lg:w-full flex xl:flex-none lg:flex-1 flex-col gap-4">
			<p class=" text-2xl font-medium text-[#252525]">Example ideas:</p>
			<div class="outline outline-1 outline-[#DEDEDE] mt-2" />
			<div class="gap-4 flex flex-col">
				<div class="flex flex-col gap-2">
					<p class="text-4 leading-6 font-medium text-[#001638]">Good explained ideas:</p>
					<div class="flex flex-col gap-1 text-[14px] leading-6 font-medium text-[#001638]">
						<div class="flex flex-row items-center justify-start pl-3 gap-3">
							<div class="w-1.5 h-1.5 bg-black rounded-full" />
							<p>Some example of a well described idea</p>
						</div>
						<div class="flex flex-row items-center justify-start pl-3 gap-3">
							<div class="w-1.5 h-1.5 bg-black rounded-full" />
							<p>Another good example of well explained idea</p>
						</div>
					</div>
				</div>
				<div class="flex flex-col gap-2">
					<p class="text-4 leading-6 font-medium text-[#001638]">Not good explained ideas:</p>
					<div class="flex flex-col gap-1 text-[14px] leading-6 font-medium text-[#001638]">
						<div class="flex flex-row items-center justify-start pl-3 gap-3">
							<div class="w-1.5 h-1.5 bg-black rounded-full" />
							<p>I want to make machine</p>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
