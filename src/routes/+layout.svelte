<script>
	import Nav from '$lib/Nav.svelte';
	import Footer from '$lib/Footer.svelte';
</script>

<main>
	<Nav />
	<slot />
	<Footer />
</main>

<style>
	:global(body) {
		font-family: 'Arial', sans-serif;
		margin: 0;
		padding: 0;
		background: linear-gradient(to bottom, hsl(0, 0%, 0%) 60%, hsl(0, 0%, 29%)) 40%;
		color: hsl(34, 78%, 91%);
	}
</style>
