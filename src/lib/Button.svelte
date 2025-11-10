<script lang="ts">
	import type { Snippet } from 'svelte';

	interface Props {
		children: Snippet;
		// must use resolve when passing href to this component
		// eslint svelte/no-navigation-without-resolve off
		href: string;
	}

	let { children, href }: Props = $props();
</script>

<!-- @component
usage
```
<Button href=resolve('/projects')>Click Me!</Button>
```
 -->
<a
	class="
   inline-block self-center rounded border border-button-secondary
   bg-button-primary px-5 py-2.5 font-medium whitespace-nowrap text-button-label
   shadow-sm transition-colors
   hover:bg-button-hover
   focus:outline-2 focus:outline-offset-2 focus:outline-button-label
   active:bg-button-hover
 "
	{href}
	tabindex="0">
	{@render children()}
</a>
