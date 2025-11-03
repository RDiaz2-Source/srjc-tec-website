<script lang="ts">
	import type { Snippet } from 'svelte';

	interface Props {
		children: Snippet;
		href: string;
	}

	let { children, href }: Props = $props();
</script>

<a
	class="
   inline-block rounded border border-button-secondary bg-button-primary px-5
   py-2.5 font-medium text-button-label shadow-sm transition-colors
   hover:bg-button-hover
   focus:outline-2 focus:outline-offset-2 focus:outline-button-label
   active:bg-button-hover
 "
	{href}
	tabindex="0">
	{@render children()}
</a>
