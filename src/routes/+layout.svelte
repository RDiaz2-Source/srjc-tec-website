<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import type { Snippet } from 'svelte';

	interface Props {
		children: Snippet;
	}

	let { children }: Props = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}

<style lang="postcss">
	@reference "tailwindcss";
</style>
