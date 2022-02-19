<script>
	import Button from '../components/Button.svelte';
</script>

<main id="main" class="grid-container">
	<div class="text-area">
		<h1 class="text-accent fs-500 ff-sans-cond uppercase letter-spacing-1">
			So, you want to travel to
			<span class="d-block fs-900 ff-serif text-white">Space</span>
		</h1>

		<p>
			Let’s face it; if you want to go to space, you might as well genuinely go to outer space and
			not hover kind of on the edge of it. Well sit back, and relax because we’ll give you a truly
			out of this world experience!
		</p>
	</div>
	<div>
		<Button href="/" type="large-button uppercase ff-serif text-dark bg-white">Explore</Button>
	</div>
</main>

<style>
	.grid-container {
		background-image: url('./home/background-home-mobile.jpg');
		background-size: cover;
		background-position: bottom center;
	}

	@media (min-width: 35em) {
		.grid-container {
			background-image: url('../../home/background-home-tablet.jpg');
			background-position: center center;
			padding-bottom: max(6rem, 15vh);
			align-items: end;
		}
	}

	@media (min-width: 45em) {
		.grid-container {
			background-image: url('../../home/background-home-desktop.jpg');
		}
	}
</style>
