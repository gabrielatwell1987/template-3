<script>
	import Title from '$lib/Title.svelte';
	import Image from '$lib/Image.svelte';
	import { onMount } from 'svelte';
	import gsap from 'gsap';

	onMount(() => {
		const image = document.querySelector('.image');

		gsap.set(image, { x: -30 });

		image.addEventListener('mouseover', () => {
			gsap.to(image, { duration: 1, scale: 1.25, x: 75 });
		});

		image.addEventListener('mouseleave', () => {
			gsap.to(image, { duration: 1, scale: 1, x: -30 });
		});
	});
</script>

<div class="title">
	<Title title="About" />
</div>

<div class="image">
	<Image
		src="https://images.unsplash.com/photo-1625662171891-9a3348f961f4?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
		alt=""
		width="35%"
	/>
</div>

<div class="content">
	<p>This is your about page. You can list things that are about you.</p>

	<div class="flex">
		<div class="left">
			<p class="left-content">
				Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestias enim possimus dolores
				molestiae dolorem eos iure aliquid tempore veniam odit natus eveniet perspiciatis nulla
				quisquam, harum doloremque expedita! Eveniet, assumenda!
			</p>
		</div>

		<div class="right">
			<p class="right-content">
				Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestias enim possimus dolores
				molestiae dolorem eos iure aliquid tempore veniam odit natus eveniet perspiciatis nulla
				quisquam, harum doloremque expedita! Eveniet, assumenda!
			</p>
		</div>
	</div>
</div>

<style>
	.content {
		margin: 3% 0 5% 33%;
		letter-spacing: 3px;
		line-height: 1.75;
	}

	.image {
		margin: 3% 0 0 39%;
	}

	.flex {
		display: flex;
		gap: 1rem;
		margin-top: 3%;
		margin-left: -15%;
	}

	.left-content {
		width: 45%;
		border: 2px solid aliceblue;
		border-radius: 0.15rem;
		padding: 1rem 1.5rem;
		font-weight: 600;
		letter-spacing: 5px;
		line-height: 1.75;
		text-align: left;
		margin-left: 10%;
	}

	.right-content {
		width: 45%;
		border: 2px solid aliceblue;
		border-radius: 0.15rem;
		padding: 1rem 1.5rem;
		font-weight: 600;
		letter-spacing: 5px;
		line-height: 1.75;
		text-align: right;
		margin-left: -18%;
	}

	.title {
		margin-left: -50%;
		margin-bottom: 15%;
	}
</style>
