<script lang="ts">
	// Props
	let { className = '' }: { className?: string } = $props();

	// State
	let isMobileMenuOpen = $state(false);

	// Functions
	function toggleMobileMenu() {
		isMobileMenuOpen = !isMobileMenuOpen;
	}
</script>

<header class="fixed inset-x-0 top-2 z-50 container {className}">
	<div class="mx-auto max-w-screen-xl">
		<div
			class="relative flex h-[58px] items-center justify-between rounded-xl bg-white/80 px-4 backdrop-blur-md"
		>
			<div class="flex-shrink-0">
				<a href="/" aria-label="Squint Home">
					<svg width="33" height="36" viewBox="0 0 33 36" fill="none" xmlns="http://www.w3.org/2000/svg">
						<rect width="33" height="36" rx="9" class="fill-secondary-600"></rect>
						<path
							d="M16.5 24.4286V10.8571M16.5 17.1428H23.7857M16.5 17.1428H9.21429"
							stroke="white"
							stroke-width="2"
							stroke-linecap="round"
						></path>
					</svg>
				</a>
			</div>

			<nav class="hidden items-center gap-2 lg:flex">
				<a
					href="#"
					class="text-level-base flex items-center gap-1 rounded-full py-1 pl-3 pr-2 font-body font-normal text-gray-700 transition-colors hover:text-primary-600"
				>
					Product
					<svg class="h-5 w-5 text-gray-500" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
						<path
							fill-rule="evenodd"
							d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z"
							clip-rule="evenodd"
						></path>
					</svg>
				</a>
				<a
					href="#"
					class="text-level-base rounded-full py-1 px-4 font-body font-normal text-gray-700 transition-colors hover:text-primary-600"
					>Enterprise</a
				>
				<a
					href="#"
					class="text-level-base rounded-full py-1 px-4 font-body font-normal text-gray-700 transition-colors hover:text-primary-600"
					>Resources</a
				>
				<a
					href="#"
					class="text-level-base rounded-full py-1 px-4 font-body font-normal text-gray-700 transition-colors hover:text-primary-600"
					>About Us</a
				>
			</nav>

			<div class="flex items-center gap-2">
				<a
					href="#"
					class="text-level-base hidden rounded-full py-1 px-4 font-body font-normal text-gray-700 transition-colors hover:text-primary-600 lg:block"
					>Log In</a
				>
				<a
					href="#"
					class="text-level-base rounded-xl bg-primary-600 p-3 font-body font-normal text-white shadow-sm transition-colors hover:bg-primary-700"
					>Request a Demo</a
				>
				<button
					type="button"
					class="rounded-md p-2 text-gray-700 hover:bg-gray-100 lg:hidden"
					onclick={toggleMobileMenu}
					aria-controls="mobile-menu"
					aria-expanded={isMobileMenuOpen}
				>
					<span class="sr-only">Open main menu</span>
					{#if isMobileMenuOpen}
						<svg
							class="h-6 w-6"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"></path>
						</svg>
					{:else}
						<svg
							class="h-6 w-6"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
							></path>
						</svg>
					{/if}
				</button>
			</div>

			{#if isMobileMenuOpen}
				<div class="absolute top-full left-0 right-0 mt-2 lg:hidden" id="mobile-menu">
					<div
						class="rounded-xl bg-white/95 p-4 shadow-lg ring-1 ring-gray-200 backdrop-blur-md"
					>
						<nav class="flex flex-col gap-2">
							<a
								href="#"
								class="text-level-xl flex items-center justify-between rounded-lg px-3 py-2 font-body font-medium text-gray-800 hover:bg-gray-100 hover:text-primary-600"
							>
								<span>Product</span>
								<svg
									class="h-5 w-5 text-gray-500"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true"
								>
									<path
										fill-rule="evenodd"
										d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z"
										clip-rule="evenodd"
									></path>
								</svg>
							</a>
							<a
								href="#"
								class="text-level-xl block rounded-lg px-3 py-2 font-body font-medium text-gray-800 hover:bg-gray-100 hover:text-primary-600"
								>Enterprise</a
							>
							<a
								href="#"
								class="text-level-xl block rounded-lg px-3 py-2 font-body font-medium text-gray-800 hover:bg-gray-100 hover:text-primary-600"
								>Resources</a
							>
							<a
								href="#"
								class="text-level-xl block rounded-lg px-3 py-2 font-body font-medium text-gray-800 hover:bg-gray-100 hover:text-primary-600"
								>About Us</a
							>
							<hr class="my-2 border-gray-200" />
							<a
								href="#"
								class="text-level-xl block rounded-lg px-3 py-2 font-body font-medium text-gray-800 hover:bg-gray-100 hover:text-primary-600"
								>Log In</a
							>
						</nav>
					</div>
				</div>
			{/if}
		</div>
	</div>
</header>