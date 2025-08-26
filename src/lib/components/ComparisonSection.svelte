<script lang="ts">
	// Types
	type ComparisonMetric = {
		title: string;
		manualDescription: string;
		squintDescription: string;
		manualValue: string;
		squintValue: string;
		manualBarClass: string;
		squintBarClass: string;
	};

	// Props
	let { className = '' }: { className?: string } = $props();

	// Static data for the comparison chart.
	// This is kept inside the component to maintain content locality, as per requirements.
	const comparisonData: ComparisonMetric[] = [
		{
			title: 'Documentation Time',
			manualDescription: 'Manual documentation takes 8+ hours per process.',
			squintDescription: 'Squint captures and generates instructions in under 15 minutes.',
			manualValue: '8+ Hours',
			squintValue: '15 Mins',
			manualBarClass: 'h-full',
			squintBarClass: 'h-6'
		},
		{
			title: 'Training Time',
			manualDescription: 'Traditional training takes 40+ hours per new hire.',
			squintDescription: 'With Squint, onboarding is 75% faster.',
			manualValue: '40+ Hours',
			squintValue: '10 Hours',
			manualBarClass: 'h-[320px]',
			squintBarClass: 'h-[80px]'
		}
	];
</script>

<section class="w-full bg-[var(--color-background)] {className}">
	<div class="container mx-auto max-w-screen-2xl">
		<div
			class="flex flex-col gap-10 rounded-[40px] border-4 border-gray-200 bg-white px-4 pb-4 pt-10 md:p-16 xl:p-20"
		>
			<header class="flex flex-col gap-10 lg:flex-row lg:items-end lg:justify-between">
				<div class="flex max-w-3xl flex-col gap-4">
					<h2 class="font-display text-level-5xl font-semibold tracking-tighter text-gray-900">
						How Squint compares to manual documentation.
					</h2>
					<p class="font-body text-level-xl font-medium text-gray-500">
						Go from process to procedure in minutes, not days. Eliminate errors and accelerate
						training.
					</p>
				</div>
				<a
					href="#"
					class="flex h-16 shrink-0 items-center justify-center gap-4 rounded-2xl bg-primary-600 px-6 no-underline transition-colors hover:bg-primary-700 font-body text-level-xl font-medium text-white"
				>
					<span>Start Automating</span>
					<span aria-hidden="true">-&gt;</span>
				</a>
			</header>

			<div class="flex flex-col border-t border-gray-200 lg:flex-row">
				{#each comparisonData as metric, i}
					<article
						class="flex flex-1 flex-col gap-10 p-6 md:p-10 lg:gap-20 lg:p-12 xl:p-20"
					>
						<header class="flex flex-col gap-2">
							<h4 class="font-display text-level-3xl font-semibold tracking-tight text-gray-800">
								{metric.title}
							</h4>
							<p class="font-body text-level-lg font-medium text-gray-700">
								<span class="text-gray-500">{metric.manualDescription}</span>
								<br />
								{metric.squintDescription}
							</p>
						</header>

						<div class="flex h-[400px] items-end justify-center gap-4">
							<!-- Manual Comparison Column -->
							<div class="flex w-1/2 flex-col items-center gap-4">
								<p class="font-body text-level-xl text-center font-medium text-gray-500">
									{metric.manualValue}
								</p>
								<div
									class="w-full border-t-4 border-gray-200 bg-gradient-to-t from-transparent to-gray-200/20 {metric.manualBarClass}"
								></div>
							</div>

							<!-- Squint Comparison Column -->
							<div class="flex w-1/2 flex-col items-center gap-4">
								<svg
									width="33"
									height="36"
									viewBox="0 0 33 36"
									fill="none"
									xmlns="http://www.w3.org/2000/svg"
									class="h-6 w-auto text-primary-500"
									aria-label="Squint logo"
								>
									<rect width="33" height="36" rx="9" fill="currentColor"></rect>
									<path
										d="M16.5 24.4286V10.8571M16.5 17.1428H23.7857M16.5 17.1428H9.21429"
										stroke="var(--color-background)"
										stroke-width="2"
										stroke-linecap="round"
									></path>
								</svg>
								<p class="font-body text-level-xl text-center font-medium text-gray-800">
									{metric.squintValue}
								</p>
								<div
									class="w-full border-t-4 border-primary-600 bg-gradient-to-t from-transparent to-primary-600/20 {metric.squintBarClass}"
								></div>
							</div>
						</div>
					</article>

					{#if i < comparisonData.length - 1}
						<div class="h-px w-full bg-gray-200 lg:h-auto lg:w-px"></div>
					{/if}
				{/each}
			</div>
		</div>
	</div>
</section>