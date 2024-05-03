<script>
	export let title;
	import { onMount } from 'svelte';
	import gsap from 'gsap';
	import SplitType from 'split-type';

	onMount(() => {
		const title = document.querySelector('h1');

		// title animation
		const text = new SplitType(title, { types: 'words, chars' });

		// Animate characters into view with a stagger effect
		gsap.from(text.chars, {
			y: -500,
			duration: 1,
			stagger: { amount: 0.75 }
		});
	});
</script>

<h1>{title}</h1>

<style>
	h1 {
		color: hsl(0, 0%, 100%);
		font-size: 5rem;
		text-align: center;
		margin-top: 5%;
		font-weight: 800;
		letter-spacing: 50px;
	}
</style>
