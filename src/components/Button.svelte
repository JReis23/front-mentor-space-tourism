<script>
	export let href = null;
	export let type = 'primary';
	export let rel = null;
	export let target = null;
	export let active = null;
</script>

{#if href}
	<a {href} class={type} {rel} {target}>
		<slot />
	</a>
{:else}
	<button class="{type} {active}" on:click>
		<slot />
	</button>
{/if}

<style>
	.large-button {
		font-size: 2rem;
		position: relative;
		z-index: 1;
		display: inline-grid;
		place-items: center;
		padding: 0 2em;
		border-radius: 50%;
		aspect-ratio: 1;
		text-decoration: none;
	}

	.large-button::after {
		content: '';
		position: absolute;
		z-index: -1;
		width: 100%;
		height: 100%;
		background: hsl(var(--clr-white) / 0.1);
		border-radius: 50%;
		opacity: 0;
		transition: opacity 500ms linear, transform 750ms ease-in-out;
	}

	.large-button:hover::after,
	.large-button:focus::after {
		opacity: 1;
		transform: scale(1.5);
	}
</style>
