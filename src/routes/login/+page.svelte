<script lang="ts">
	import Hero from '$lib/components/LandingPage/Hero.svelte'
	import Utility from '$lib/components/LandingPage/Utility/Utility.svelte'
	import Partnerships from '$lib/components/LandingPage/Partnerships/Partnerships.svelte'
	import Roadmap from '$lib/components/LandingPage/Roadmap/Roadmap.svelte'
	import Team from '$lib/components/LandingPage/Team/Team.svelte'

	import heroText from '$lib/assets/images/login-web3-title.webp'
	import poweredByIcon from '$lib/assets/images/solana.svg'
</script>

<Hero {heroText} {poweredByIcon} />
<Utility />
<Partnerships />
<Roadmap />
<Team />
