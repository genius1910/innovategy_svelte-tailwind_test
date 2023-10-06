<script>
	import logo from '$lib/images/logo.svg';
	import bg from '$lib/images/bg.svg';
</script>

<div class="flex w-screen h-screen bg-white">
	<div class="hidden md:block w-1/2 bg-[#FAFAFA] relative">
		<div class="pt-10 pl-7">
			<img src={logo} alt="SvelteKit" />
		</div>
		<div class="xl:flex hidden pl-[100px] pt-11 flex-col gap-3">
			<span class="text-[#001638] text-2xl font-medium leading-8">
				Donec aliquam ex sed neque eleifend
			</span>
			<span class="text-[#001638] text-sm font-normal leading-6">
				Donec aliquam ex sed neque eleifend elementum
			</span>
		</div>
		<div
			class="xl:block hidden absolute bottom-0 left-24 right-0 border-t-[16px] border-l-[16px] border-[#001638] rounded-tl-[32px]"
		>
			<img src={bg} alt="Bg" />
		</div>
	</div>
	<div
		class="w-full xl:w-1/2 flex flex-col gap-10 items-center justify-center xl:pl-[106px] xl:pr-[158px] pl-[54px] pr-[78px] relative"
	>
		<div class="pt-10 pl-7 absolute top-0 left-0 md:hidden">
			<img src={logo} alt="SvelteKit" />
		</div>
		<div class="relative flex flex-col gap-10 items-center justify-center w-full">
			<div class="flex flex-col gap-2 w-full">
				<span class="text-[#001638] text-[32px] font-medium leading-[48px]">
					Log in to Innovategy OY
				</span>
				<span class="text-[#666] text-[14px] font-normal leading-[24px]">
					Enter your credentials to acces your account
				</span>
			</div>
			<form class="flex flex-col gap-6 w-full" action="/dashboard">
				<div class="flex flex-col gap-2 w-full">
					<span class="text-[#001638] text-[14px] font-normal leading-[24px]">
						Email address
					</span>
					<input
						type="email"
						class="px-4 py-3 border border-[#CACFD5] text-[#001638] text-[14px] font-normal leading-[24px] placeholder:{'text-[#7D8899]'} focus:outline-none rounded-lg"
						placeholder="name@company.com"
					/>
				</div>
				<div class="flex flex-col gap-2 w-full">
					<span class="text-[#001638] text-[14px] font-normal leading-[24px]">
						Password
					</span>
					<input
						type="password"
						class="px-4 py-3 border border-[#CACFD5] text-[#001638] text-[14px] font-normal leading-[24px] placeholder:{'text-[#7D8899]'} focus:outline-none rounded-lg"
						placeholder="Placeholder"
					/>
				</div>
				<div class="flex flex-row gap-2 w-full">
					<input type="checkbox" />
					<span class="text-[#001638] text-[14px] font-normal leading-[24px]">
						Remember information
					</span>
				</div>
				<div>
					<input
						type="submit"
						class="px-4 py-3 bg-[#0CBFAD] hover:bg-[#0cbfadda] duration-500 text-white text-[14px] font-medium leading-[24px] rounded-lg w-full cursor-pointer"
						value="Login"
					/>
				</div>
			</form>
		</div>
		<div class="w-full">
			<span
				class="text-[#001638] text-[14px] font-normal leading-[24px] text-start w-full"
			>
				Not a member? <a href="/signup" class="text-[#0CBFAD]">Sign up now</a>
			</span>
		</div>
	</div>
</div>
