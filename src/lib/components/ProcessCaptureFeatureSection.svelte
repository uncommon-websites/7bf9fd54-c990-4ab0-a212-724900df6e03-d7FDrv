<script lang="ts">
	// Types for the gallery items and columns
	type ProcessItem = {
		imgSrc: string;
		altText: string;
		title: string;
		source: string;
	};

	type GalleryColumn = {
		className: string;
		items: ProcessItem[];
	};

	// Props
	let { className = '' }: { className?: string } = $props();

	// State
	// Using $state.raw as the gallery data is static and won't change at runtime.
	// This is more performant than a fully reactive state object.
	const galleryColumns: GalleryColumn[] = $state.raw([
		{
			className: 'flex flex-col gap-2 pt-6 sm:gap-6',
			items: [
				{
					imgSrc: 'https://www.ledr.com/colours/black.jpg',
					altText: 'A video of a machine calibration process.',
					title: 'Machine Calibration',
					source: 'Captured from video'
				},
				{
					imgSrc: 'https://www.ledr.com/colours/black.jpg',
					altText: 'A screen recording of an ERP software task.',
					title: 'Work Order Entry',
					source: 'Captured from screen recording'
				}
			]
		},
		{
			className: 'flex flex-col gap-2 pt-16 sm:gap-6 sm:pt-20 lg:pt-40',
			items: [
				{
					imgSrc: 'https://www.ledr.com/colours/black.jpg',
					altText: 'A video of a quality inspection procedure.',
					title: 'Quality Inspection',
					source: 'Captured from mobile device'
				},
				{
					imgSrc: 'https://www.ledr.com/colours/black.jpg',
					altText: 'A video showing a safety protocol.',
					title: 'Lockout/Tagout Procedure',
					source: 'Captured from video'
				}
			]
		},
		{
			className: 'hidden flex-col gap-2 pt-6 sm:gap-6 lg:flex',
			items: [
				{
					imgSrc: 'https://www.ledr.com/colours/black.jpg',
					altText: 'A video of a complex assembly process.',
					title: 'Sub-Assembly Build',
					source: 'Captured from headset'
				},
				{
					imgSrc: 'https://www.ledr.com/colours/black.jpg',
					altText: 'A screen recording of a maintenance log entry.',
					title: 'Maintenance Log',
					source: 'Captured from screen recording'
				}
			]
		},
		{
			className: 'hidden flex-col gap-2 pt-16 sm:gap-6 sm:pt-20 lg:pt-40 xl:flex',
			items: [
				{
					imgSrc: 'https://www.ledr.com/colours/black.jpg',
					altText: 'A video of a packaging and shipping process.',
					title: 'Packaging & Shipping',
					source: 'Captured from video'
				},
				{
					imgSrc: 'https://www.ledr.com/colours/black.jpg',
					altText: 'A video of a tool changeover on a machine.',
					title: 'Tool Changeover',
					source: 'Captured from video'
				}
			]
		}
	]);
</script>

<style>
	@theme inline {
		--color-background: color-mix(in oklch, var(--color-primary-50) 55%, white);
	}
</style>

<section class="container {className}">
	<div class="bg-[var(--color-background)] py-16 sm:py-24 lg:py-32">
		<div class="flex w-full flex-col items-center gap-10 lg:gap-28">
			<div class="flex w-full max-w-7xl flex-col items-start gap-6 lg:gap-10">
				<div class="flex w-full max-w-2xl flex-col items-start gap-4 lg:gap-10">
					<h2
						class="font-display text-level-5xl font-semibold tracking-tight text-gray-900 lg:tracking-[-0.04em]"
					>
						Capture any process, instantly.<br />No typing required.
					</h2>
					<div class="font-body space-y-5 text-level-xl font-medium text-gray-700">
						<p>
							Squint's computer vision automatically captures your team's expertise. Simply record a
							video of any task, and Squint transforms it into clear, visual instructions.
						</p>
						<p>
							Overcome documentation resistance and capture tribal knowledge as it happens, without
							interrupting the workflow of your most valuable experts.
						</p>
					</div>
				</div>
				<div class="flex flex-col gap-2 sm:flex-row sm:gap-6">
					<a
						href="#"
						class="font-body flex h-12 items-center justify-center gap-4 rounded-2xl border border-gray-200 bg-white px-6 py-1 text-level-xl font-medium text-gray-800 transition-transform hover:scale-105 hover:bg-gray-50 lg:h-16"
					>
						<span>See How It Works</span>
						<span aria-hidden="true">-&gt;</span>
					</a>
					<a
						href="#"
						class="font-body flex h-12 items-center justify-center gap-4 rounded-2xl bg-primary-600 px-6 py-1 text-level-xl font-medium text-white transition-transform hover:scale-105 hover:bg-primary-700 lg:h-16"
					>
						<span>Request a Demo</span>
						<span aria-hidden="true">-&gt;</span>
					</a>
				</div>
			</div>

			<div class="grid w-full grid-cols-2 gap-2 sm:gap-6 lg:grid-cols-3 xl:grid-cols-4">
				{#each galleryColumns as column}
					<div class={column.className}>
						{#each column.items as item}
							<div
								class="relative aspect-[9/10] w-full overflow-hidden rounded-[17px] bg-white p-1 shadow-sm sm:rounded-[32px] sm:p-4"
							>
								<img
									src={item.imgSrc}
									alt={item.altText}
									class="h-full w-full rounded-xl object-cover sm:rounded-3xl"
								/>
								<div
									class="absolute inset-x-2 bottom-2 flex items-center justify-between rounded-xl bg-white/80 p-3 backdrop-blur-md sm:inset-x-4 sm:bottom-4 sm:rounded-2xl sm:p-4"
								>
									<div class="flex flex-col">
										<p class="font-body text-level-sm font-medium leading-tight text-gray-900">
											{item.title}
										</p>
										<p class="font-body text-level-xs leading-tight text-gray-500">
											{item.source}
										</p>
									</div>
									<div
										class="flex h-6 w-6 shrink-0 items-center justify-center rounded-lg bg-white sm:h-8 sm:w-8"
									>
										<span class="font-body text-level-lg font-medium text-primary-600">-&gt;</span>
									</div>
								</div>
							</div>
						{/each}
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>