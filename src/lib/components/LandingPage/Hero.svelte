<script lang="ts">
	import LinkPrimaryButton from '$lib/components/LandingPage/Button/LinkPrimaryButton.svelte'
	import LinkOutlineButton from '$lib/components/LandingPage/Button/LinkOutlineButton.svelte'

	import discordIcon from '$lib/assets/images/discord-white.svg'
	import discordTextIcon from '$lib/assets/images/discord-text.svg'
	import whitepaperIcon from '$lib/assets/images/whitepaper.svg'

	export let heroText: string, poweredByIcon: string
</script>

<div class="bg-hero bg-cover bg-no-repeat bg-[#25252A] relative overflow-hidden">
	<div
		class="container relative space-y-20 mb-20 sm:space-y-24 sm:my-24 lg:space-y-32 lg:my-32 ml-auto mr-auto">
		<div class="relative pb-10 pl-[54px] pt-24">
			<div
				class="flex flex-col lg:flex-row space-y-14 lg:space-y-0 lg:space-x-10 lg:items-center relative">
				<div class="w-screen max-w-full xl:max-w-xl space-y-5 lg:space-y-7">
					<img src={heroText} class="md:w-[80%] sm:w-[60%] max-w-[80%]" alt="Web3-Text" />
					<span class="block text-lg xl:text-xl text-white font-medium max-w-lg">
						Code Crow is a Web3 <span class="text-[#EC008C]">Stream-and-Earn</span> platform for gamers
						and developers
					</span>
					<span class="flex space-x-4 text-lg xl:text-xl text-white font-medium max-w-lg">
						<span>Powered by</span>
						<img src={poweredByIcon} alt="" />
					</span>
					<div class="flex space-x-8">
						<LinkPrimaryButton
							title="Join our"
							link="https://discord.com/invite/CodeCrow"
							bgColor="bg-[#5765f1] hover:bg-[#5765f1]"
							border="border-1 border-[#5765f1] hover:border-[#5765f1]"
							startIcon={discordIcon}
							endIcon={discordTextIcon}
							optionalClass="w-[270px] uppercase"
							targetBlank={true} />
						<LinkOutlineButton
							title="Read Whitepaper"
							link="https://code-crow.gitbook.io/whitepaper/"
							titleColor="text-white"
							border="border-1 border-white hover:border-white"
							startIcon={whitepaperIcon}
							optionalClass="w-[270px] uppercase"
							targetBlank={true} />
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
