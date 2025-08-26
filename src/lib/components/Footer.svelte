<script lang="ts">
	// Props
	let { className = '' }: { className?: string } = $props();
</script>

<footer class="container bg-[var(--color-background)] {className}">
	<div class="flex flex-col pt-20 pb-16 md:pt-36 md:pb-10">
		<div class="flex flex-col gap-16 md:gap-20">
			<div>
				<svg
					class="h-auto w-full text-gray-200"
					viewBox="0 0 1316 160"
					fill="none"
					xmlns="http://www.w3.org/2000/svg"
					aria-hidden="true"
				>
					<path
						d="M1316 1C1316 1 1184.28 160 658 160C131.72 160 1 1 1 1"
						stroke="currentColor"
						stroke-width="2"
					></path>
				</svg>
			</div>
			<div class="flex flex-col gap-12 md:flex-row md:items-start md:justify-between">
				<a href="/" aria-label="Squint Home">
					<!-- NOTE: This logo is white and may not be visible on a light background. A dark version of the logo is recommended. -->
					<img
						src="https://www.ledr.com/colours/white.jpg"
						alt="Squint Logo"
						class="h-[46px] w-[42px]"
					/>
				</a>

				<nav class="flex flex-col gap-7 md:flex-row md:gap-20">
					<div class="flex flex-col gap-2.5">
						<p class="font-display text-level-xs text-gray-500">Product</p>
						<a href="/" class="font-body text-level-lg text-gray-700 hover:text-primary-600">
							Visual Capture
						</a>
						<a href="/" class="font-body text-level-lg text-gray-700 hover:text-primary-600">
							AI-Generated Guides
						</a>
						<a href="/" class="font-body text-level-lg text-gray-700 hover:text-primary-600">
							Enterprise Plan
						</a>
					</div>
					<div class="flex flex-col gap-2.5">
						<p class="font-display text-level-xs text-gray-500">Company</p>
						<a href="/" class="font-body text-level-lg text-gray-700 hover:text-primary-600">
							Resources
						</a>
						<a href="/" class="font-body text-level-lg text-gray-700 hover:text-primary-600">
							About Us
						</a>
						<a href="/" class="font-body text-level-lg text-gray-700 hover:text-primary-600">
							Careers
						</a>
					</div>
					<div class="flex flex-col gap-2.5">
						<p class="font-display text-level-xs text-gray-500">Legal</p>
						<a href="/" class="font-body text-level-lg text-gray-700 hover:text-primary-600">
							Terms of service
						</a>
						<a href="/" class="font-body text-level-lg text-gray-700 hover:text-primary-600">
							Privacy policy
						</a>
					</div>
				</nav>
			</div>
		</div>
	</div>
</footer>

<style>
	@theme inline {
		--color-background: color-mix(in oklch, var(--color-primary-50) 55%, white);
	}
</style>