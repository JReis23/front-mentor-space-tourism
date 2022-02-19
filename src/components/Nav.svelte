<script>
	let open = false;
</script>

<header class="primary-header flex">
	<div>
		<img src="../../shared/logo.svg" alt="space tourism logo" class="logo" />
	</div>
	<button
		on:click={() => (open = !open)}
		class="mobile-nav-toggle {open === true ? 'mobile-nav-toggle-open' : null}"
		aria-controls="primary-navigation"><span class="sr-only">Menu</span></button
	>
	<nav>
		<ul
			id="primary-navigation"
			class="primary-navigation {open === true
				? 'primary-navigation-open'
				: null} underline-indicators flex"
		>
			<li class="active">
				<a class="ff-sans-cond uppercase text-white letter-spacing-2" href="../../"
					><span aria-hidden="true">00</span>Home</a
				>
			</li>
			<li>
				<a class="ff-sans-cond uppercase text-white letter-spacing-2" href="../destination"
					><span aria-hidden="true">01</span>Destination</a
				>
			</li>
			<li>
				<a class="ff-sans-cond uppercase text-white letter-spacing-2" href="../../crew/commander"
					><span aria-hidden="true">02</span>Crew</a
				>
			</li>
			<li>
				<a
					class="ff-sans-cond uppercase text-white letter-spacing-2"
					href="../../technology/vehicle"><span>03</span>Technology</a
				>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		position: fixed;
		min-width: 100%;
		z-index: 3333;
	}

	@media (max-width: 35rem) {
		.primary-navigation-open {
			transform: translate(0%);
		}

		.mobile-nav-toggle-open {
			background-image: url(../../shared/icon-close.svg);
		}

		.mobile-nav-toggle-open:focus-visible {
			outline-offset: 5px;
			outline: 5px solid white;
		}
	}

	@media (min-width: 45em) {
		.primary-header::before {
			content: '';
			display: block;
			position: relative;
			height: 1px;
			width: 100%;
			background: hsl(var(--clr-light));
			order: 2;
			margin-right: -5%;
			margin-left: 5%;
			z-index: 212;
		}

		header > div {
			order: 1;
		}

		header > nav {
			order: 3;
		}

		.primary-navigation {
			margin-block: 2rem;
		}
	}
</style>
