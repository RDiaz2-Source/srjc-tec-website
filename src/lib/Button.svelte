<script lang="ts">
	import type { Snippet } from 'svelte';

	interface Props {
		children: Snippet;
	}

	let { children }: Props = $props();
</script>

<div
	class="
   inline-flex flex-col items-center justify-center overflow-hidden rounded-md
   bg-button-primary p-2
   md:overflow-hidden
   lg:overflow-hidden
 "
>
	<div
		class="
    justify-center font-['Inter'] text-base leading-7 font-semibold text-black
    md:text-lg
  "
	>
		{@render children()}
	</div>
</div>
