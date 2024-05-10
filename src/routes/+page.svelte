<script>
	import Title from '$lib/Title.svelte';
	import Image from '$lib/Image.svelte';
	import { onMount } from 'svelte';
	import gsap from 'gsap';

	onMount(() => {
		const title = document.querySelector('.title');
		const content = document.querySelector('.content');
		const img = document.querySelector('.img');

		gsap.set([title, content, img], { opacity: 1 });
		gsap.set(img, { x: 0, y: -120 });

		const tl = gsap.timeline({ defaults: { ease: 'expo' } });
		tl.from(title, { duration: 2.5, x: 100, opacity: 0 })
			.from(content, { duration: 2, x: 100, opacity: 0 })
			.from(img, {
				duration: 3,
				scale: 1.25,
				x: 0,
				y: 0,
				opacity: 0,
				transformOrigin: 'center center'
			});
	});
</script>

<div class="title">
	<Title title="The Title" />
</div>

<div class="content">
	<p>This is where your content goes. You can add as much content as you want.</p>

	<p>
		Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloremque expedita debitis pariatur
		totam quidem quas? Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iste blanditiis
		rerum eaque laborum similique quo itaque maiores praesentium illo veritatis?
	</p>
</div>

<div class="image">
	<div class="img">
		<Image
			src="https://images.unsplash.com/photo-1530435460869-d13625c69bbf?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
			alt=""
			width="30%"
		/>
	</div>
</div>

<style>
	p {
		margin: 3% 0 3% 45%;
		letter-spacing: 5px;
		line-height: 1.75;
		font-size: 1.1rem;
		font-weight: 300;
		width: 50%;
	}

	.content {
		margin-top: -1%;
	}

	.image {
		position: relative;
		width: 75%;
	}

	.img {
		height: auto;
		position: absolute;
		top: -180px;
		left: 250px;
		border-radius: 0.25rem;
	}
	.title {
		margin-bottom: 12%;
	}
</style>
