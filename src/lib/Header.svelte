<script lang="ts">
	import NavBar from './NavBar.svelte';
	import NavButtonIcon from '$lib/icons/nav-button.svg?component';

	const tabs = ['About', 'Contact', 'Projects'];
</script>

<header class="border-b-2 border-b-black bg-white">
	<div
		class="
    mx-auto max-w-7xl px-4
    sm:px-6
    lg:px-8
  ">
		<div class="flex h-16 items-center justify-between">
			<div
				class="
      flex-1
      md:flex md:items-center md:gap-12
    ">
				<a class="block text-red-400" href="#">
					<span class="sr-only">Home</span>
					Logo
					<span class="text-lg font-semibold text-black">TEC</span>
				</a>
			</div>

			<div class="md:flex md:items-center md:gap-12">
				<nav
					aria-label="Main"
					class="
       hidden
       md:block
     ">
					<ul class="flex items-center gap-6 text-sm">
						{#each tabs as label (label)}
							<li>
								<a
									class="
           text-gray-500 transition
           hover:text-gray-500/75
         "
									href="#">
									{label}
								</a>
							</li>
						{/each}
					</ul>
				</nav>

				<div class="flex items-center gap-4">
					<div class="sm:flex sm:gap-4">
						<div
							class="
         hidden
         sm:flex
       ">
							<a
								class="
          rounded-md bg-button-primary px-5 py-2.5 text-sm font-medium
          text-black
        "
								href="#">
								Join Us
							</a>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</header>
