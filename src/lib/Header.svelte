<script lang="ts">
	import { resolve } from '$app/paths';
	import Button from './Button.svelte';

	const tabs: string[] = ['About', 'Events', 'Team', 'Sponsors', 'Projects'];
</script>

<header class="bg-header">
	<div
		class="
    mx-auto max-w-7xl px-4
    sm:px-6
    lg:px-8
  ">
		<div class="flex h-16 items-center justify-between">
			<div
				class="
      flex flex-1 items-center gap-4
      md:gap-12
    ">
				<a class="block text-brand" href="#">
					<span class="sr-only">Home</span>
					Logo
					<span class="text-lg font-semibold text-header-content">TEC</span>
				</a>
			</div>

			<div
				class="
      flex items-stretch gap-4 self-stretch
      md:gap-12
    ">
				<nav aria-label="Main" class="block">
					<ul class="flex size-full items-stretch text-sm">
						{#each tabs as label (label)}
							<li>
								<a
									class="
           flex h-full items-center px-1 text-nav-tab-label transition
           hover:bg-nav-tab-hover
           active:bg-nav-tab-hover
           sm:px-2
           md:px-4
         "
									href="#">
									{label}
								</a>
							</li>
						{/each}
					</ul>
				</nav>
				<div class="
      hidden self-center
      sm:block
    ">
					<Button href={resolve('/')}>Join Us</Button>
				</div>
			</div>
		</div>
	</div>
</header>
