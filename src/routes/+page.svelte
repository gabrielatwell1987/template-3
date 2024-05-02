<script>
	import Title from '$lib/Title.svelte';
	import Image from '$lib/Image.svelte';
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
		margin: 5% 0 3% 50%;
		letter-spacing: 3px;
		line-height: 1.75;
	}

	.image {
		position: relative;
	}

	.img {
		height: auto;
		position: absolute;
		top: -325px;
		left: 250px;
		border-radius: 0.25rem;
	}
	.title {
		margin-bottom: 12%;
	}
</style>
