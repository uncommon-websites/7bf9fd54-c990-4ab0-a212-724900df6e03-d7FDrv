<script lang="ts">
	// Types
	type Logo = {
		src: string;
		alt: string;
	};

	type IntegrationCategory = {
		title: string;
		description: string;
		logos: Logo[];
	};

	// Props
	let { className = '' }: { className?: string } = $props();

	// State
	const integrationCategories: IntegrationCategory[] = $state.raw([
		{
			title: 'ERP Systems',
			description: 'Connect with SAP, Oracle, and other ERPs to link instructions directly to work orders.',
			logos: [
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'ERP System Logo 1' },
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'ERP System Logo 2' },
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'ERP System Logo 3' },
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'ERP System Logo 4' }
			]
		},
		{
			title: 'Quality Management Systems',
			description: 'Embed procedures into your QMS to ensure compliance and quality.',
			logos: [
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'QMS Logo 1' },
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'QMS Logo 2' },
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'QMS Logo 3' },
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'QMS Logo 4' }
			]
		},
		{
			title: 'Existing Documentation',
			description: 'Import and enhance your existing Word docs, PDFs, and videos.',
			logos: [
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'Doc Type Logo 1' },
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'Doc Type Logo 2' },
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'Doc Type Logo 3' },
				{ src: 'https://www.ledr.com/colours/black.jpg', alt: 'Doc Type Logo 4' }
			]
		}
	]);
</script>

<section class="container bg-[var(--color-background)] py-20 sm:py-28 {className}">
	<div class="flex flex-col gap-10 lg:flex-row lg:items-end lg:justify-between">
		<div class="max-w-xl">
			<h2 class="font-display text-level-5xl font-light text-gray-900">
				Trusted by leading <span class="text-gray-500">manufacturing teams</span>
			</h2>
		</div>
		<p class="font-body max-w-xl text-level-xl text-gray-700 lg:max-w-sm">
			Squint works with the tools you already use to streamline knowledge sharing.
		</p>
	</div>

	<div class="mt-16 flex flex-col gap-12 sm:mt-20 lg:mt-24">
		{#each integrationCategories as category}
			<div class="flex flex-col items-center gap-8 text-center">
				<div class="max-w-2xl">
					<h3 class="font-display text-level-3xl font-light text-gray-800">
						{category.title}
					</h3>
					<p class="font-body mt-4 text-level-xl text-gray-500">
						{category.description}
					</p>
				</div>
				<div class="w-full overflow-hidden rounded-2xl border border-gray-200 bg-white shadow-sm">
					<div class="flex flex-col divide-y divide-gray-200 sm:flex-row sm:divide-x sm:divide-y-0">
						{#each category.logos as logo}
							<div class="flex flex-1 items-center justify-center p-8">
								<img src={logo.src} alt={logo.alt} class="h-12 w-auto opacity-70" />
							</div>
						{/each}
					</div>
				</div>
			</div>
		{/each}
	</div>
</section>

@theme inline {
	--color-background: color-mix(in oklch, var(--color-primary-50) 55%, white);
}