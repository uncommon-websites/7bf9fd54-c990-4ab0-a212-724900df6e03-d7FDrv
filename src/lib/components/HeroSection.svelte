<script lang="ts">
	// Types
	type ImageItem = {
		src: string;
		alt: string;
		className: string;
	};

	// Props
	let { className = '' }: { className?: string } = $props();

	// State (non-reactive constant data for the image collage)
	const images: ImageItem[] = [
		{
			src: 'https://www.ledr.com/colours/black.jpg',
			alt: 'A manufacturing worker performing a complex assembly task.',
			className:
				'absolute top-[27%] left-[18%] aspect-square w-[36%] -translate-x-1/2 -translate-y-1/2 transform rounded-2xl border border-gray-200/50 bg-white shadow-2xl md:top-[50%] md:left-[11%] md:w-[22%] md:rounded-3xl'
		},
		{
			src: 'https://www.ledr.com/colours/black.jpg',
			alt: 'A factory floor with automated machinery in operation.',
			className:
				'absolute top-[27%] left-[48%] aspect-square w-[36%] -translate-x-1/2 -translate-y-1/2 transform rounded-2xl border border-gray-200/50 bg-white shadow-2xl md:top-[50%] md:left-[30%] md:w-[22%] md:rounded-3xl'
		},
		{
			src: 'https://www.ledr.com/colours/black.jpg',
			alt: 'An operations manager reviewing a process on a tablet.',
			className:
				'absolute top-[27%] left-[80%] aspect-square w-[36%] -translate-x-1/2 -translate-y-1/2 transform rounded-2xl border border-gray-200/50 bg-white shadow-2xl md:top-[50%] md:left-[50%] md:w-[22%] md:rounded-3xl'
		},
		{
			src: 'https://www.ledr.com/colours/black.jpg',
			alt: 'A close-up of a complex mechanical part being assembled.',
			className:
				'absolute top-[74%] left-[32%] aspect-square w-[36%] -translate-x-1/2 -translate-y-1/2 transform rounded-2xl border border-gray-200/50 bg-white shadow-2xl md:top-[51%] md:left-[70%] md:w-[22%] md:rounded-3xl'
		},
		{
			src: 'https://www.ledr.com/colours/black.jpg',
			alt: 'A team of engineers collaborating on a factory floor.',
			className:
				'absolute top-[72%] left-[63%] aspect-square w-[36%] -translate-x-1/2 -translate-y-1/2 transform rounded-2xl border border-gray-200/50 bg-white shadow-2xl md:top-[47%] md:left-[89%] md:w-[22%] md:rounded-3xl'
		}
	];
</script>

<section class="overflow-hidden bg-[var(--color-background)] {className}">
	<div
		class="container mx-auto flex max-w-7xl flex-col items-center justify-center gap-16 px-4 py-24 md:gap-20 lg:py-32"
	>
		<div class="flex flex-col items-center gap-8 pt-20 text-center">
			<div class="flex flex-col items-center gap-4 md:gap-6">
				<h1
					class="font-display text-level-5xl font-semibold tracking-tight text-gray-900 lg:tracking-[-0.03em]"
				>
					Documenting work was never<br />meant to be hard.
				</h1>
				<p class="font-body text-level-2xl max-w-3xl font-medium tracking-tight text-gray-700">
					Capture and standardize complex processes, automatically.
					<br class="hidden sm:block" />
					Reduce training time and production delays instantly.
				</p>
			</div>
			<a
				href="#"
				class="font-body text-level-xl group inline-flex h-16 items-center justify-center gap-4 rounded-2xl bg-primary-600 px-6 py-1 font-medium text-white transition hover:scale-105 hover:bg-primary-700"
			>
				<span
					class="text-level-2xl flex h-8 w-8 items-center justify-center rounded-lg bg-white text-primary-600"
				>
					→
				</span>
				<span>Request a Demo</span>
			</a>
		</div>

		<div class="relative aspect-[1.4/1] w-full max-w-sm md:aspect-[4.07/1] md:max-w-7xl">
			{#each images as image}
				<div class={image.className}>
					<img
						src={image.src}
						alt={image.alt}
						class="h-full w-full rounded-2xl object-cover md:rounded-3xl"
					/>
				</div>
			{/each}
		</div>
	</div>
</section>