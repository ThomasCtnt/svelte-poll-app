<script>
	import Header from './components/Header.svelte';
	import Footer from './components/Footer.svelte';
	import PollForm from './components/PollForm.svelte';
	import Tabs from './shared/Tabs.svelte';

	// Tabs
	let items = ['Current Polls', 'Add New Poll'];
	let activeItem = 'Current Polls';

	const tabSetActive = (e) => {
		activeItem = e.detail;
	}
</script>

<Header />
<main>
	<Tabs {items} {activeItem} on:tabChange={tabSetActive} />

	{#if activeItem === 'Current Polls'}
		Hello there nothing to see right now
	{:else if activeItem === 'Add New Poll'}
		<PollForm />
	{/if}
</main>
<Footer />

<style>
	main {
		max-width: 960px;
		margin: 40px auto;
	}
</style>