<script lang="ts">
	export let src;
	export let size = '100%';
	export let filled = false;
	let customClass = '';
	export { customClass as class };
	export let ariaHidden = false;

	if (size !== '100%') {
		if (size.slice(-1) != 'x' && size.slice(-1) != 'm' && size.slice(-1) != '%') {
			try {
				size = parseInt(size) + 'px';
			} catch (error) {
				size = '100%';
			}
		}
	}
</script>

<svg
	class={customClass}
	aria-hidden={ariaHidden}
	width={size}
	fill="currentColor"
	height={size}
	xmlns="http://www.w3.org/2000/svg"
	viewBox="0 0 24 24"
>
	<g>
		{#if src.length > 1}
			{#if filled}
				{#each src[0] as att}
					<path {...att} />
				{/each}
			{:else}
				{#each src[1] as att}
					<path {...att} />
				{/each}
			{/if}
		{:else}
			{#each src[0] as att}
				<path {...att} />
			{/each}
		{/if}
	</g>
</svg>
