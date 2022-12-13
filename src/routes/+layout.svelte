<script>
	import Header from '$lib/components/UI/Header.svelte';
	import Footer from '$lib/components/UI/Footer.svelte';

	import './styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<Footer />
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		width: 100%;
		box-sizing: border-box;
	}
</style>
