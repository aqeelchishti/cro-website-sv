<script>
	import Header from '$lib/components/LandingPage/Header.svelte'
	import Footer from '$lib/components/LandingPage/Footer.svelte'
	import LoginCard from '$lib/components/LandingPage/Login/LoginCard.svelte'

	import { classList } from 'svelte-body'

	// From Store
	import { isOpenLoginDialog } from '$lib/stores/store'

	/*
	const handleOpenLoginDialog = (e) => {
		isOpenLoginDialog.update(() => e.detail.isOpenLoginDialog)
	}*/
</script>

<svelte:body
	use:classList={$isOpenLoginDialog == true
		? 'overflow-hidden h-screen'
		: 'scrollbar-thin scrollbar-thumb-[#aeaeae] scrollbar-track-[#25252A] scrollbar-thumb-rounded'} />

<div>
	<Header on:open={(e) => isOpenLoginDialog.update(() => e.detail.isOpenLoginDialog)} />

	<slot />

	<Footer />
</div>

<LoginCard isOpenLoginDialogProp={$isOpenLoginDialog} />

<!--onClickDismisDialogProp={() => isOpenLoginDialog.update(() => false)}-->
