<script>
	import Title from '$lib/Title.svelte';
	import Image from '$lib/Image.svelte';
</script>

<div class="title">
	<Title title="Contact" />
</div>

<main>
	<div class="content">
		<p>This is where your contact information goes. You can add as much content as you want.</p>

		<a href="mailto:example@example.com">Email</a>
	</div>

	<div class="image">
		<div class="img">
			<Image
				src="https://images.unsplash.com/photo-1586769852044-692d6e3703f0?q=80&w=1887&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
				alt=""
				width="50%"
			/>
		</div>
	</div>
</main>

<style>
	p {
		margin: 8% 0 5% 5%;
		letter-spacing: 3px;
		line-height: 1.75;
		width: 35%;
	}

	main {
		margin: 6% 0 0 15%;
	}

	.content {
		margin-top: 6%;
	}

	.image {
		position: relative;
		margin-top: 6%;
	}

	.img {
		width: 30%;
		height: auto;
		position: absolute;
		top: -225px;
		right: 250px;
		border-radius: 0.25rem;
	}

	a {
		color: hsl(0, 0%, 100%);
		font-size: 1.5rem;
		text-align: center;
		margin-top: 5%;
		margin-left: 33%;
		font-weight: 800;
		letter-spacing: 5px;
		text-decoration: none;
	}

	a:hover {
		color: #ccc;
	}

	.title {
		margin-left: 16%;
		margin-bottom: 15%;
	}
</style>
