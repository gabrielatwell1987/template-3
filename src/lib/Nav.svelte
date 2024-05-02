<script>
	import Logo from '$lib/Logo.svelte';
</script>

<nav>
	<Logo />

	<ul>
		<li><a href="/">Home</a></li>
		<li><a href="/about">About</a></li>
		<li><a href="/contact">Contact</a></li>
	</ul>
</nav>

<style>
	nav {
		background-color: transparent;
		padding: 1rem;
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 30%;
		margin-top: 1%;
		margin-left: 10%;
	}

	ul {
		display: flex;
		gap: 20%;
		list-style: none;
		padding: 0;
		justify-content: flex-end;
		margin-right: 10%;
	}

	li {
		font-size: 1.5rem;
		transition:
			transform 0.3s ease,
			text-decoration 0.3s ease;
	}

	li:hover {
		transform: scale(1.1);
		text-decoration: underline;
	}

	a {
		text-decoration: none;
		color: hsl(0, 1%, 52%);
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 5px;
	}

	a:hover {
		color: hsl(0, 0%, 100%);
	}
</style>
