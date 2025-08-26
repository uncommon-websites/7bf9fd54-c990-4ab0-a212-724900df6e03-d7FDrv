<script lang="ts">
	// Props
	let { className = '' }: { className?: string } = $props();
</script>

<section class={`container mx-auto bg-[var(--color-background)] ${className}`}>
	<div class="flex flex-col items-start justify-center lg:flex-row">
		<!-- Column 1: Expert on Demand -->
		<div class="flex w-full flex-col items-start gap-4 p-6 md:px-10 lg:flex-1 lg:gap-6 lg:px-16 lg:py-10">
			<h4
				class="font-display text-level-4xl font-semibold leading-[1.2] tracking-[-0.4px] text-gray-900 md:tracking-[-0.5px] lg:tracking-[-1px]"
			>
				Your team's expert, on demand.<br class="hidden lg:block" />Instantly documented.
			</h4>
			<p class="font-body text-level-xl w-full font-medium leading-[1.4] tracking-tight text-gray-700">
				Squint manages your entire knowledge capture process. Automatically record, document, and
				share complex assembly procedures with visual, step-by-step instructions, freeing up your
				most experienced team members.
			</p>
		</div>

		<!-- Divider -->
		<div class="h-px w-full bg-gray-200 lg:h-auto lg:w-px lg:self-stretch"></div>

		<!-- Column 2: Eliminate Delays -->
		<div class="flex w-full flex-col items-start gap-4 p-6 md:px-10 lg:flex-1 lg:gap-6 lg:px-16 lg:py-10">
			<h4
				class="font-display text-level-4xl font-semibold leading-[1.2] tracking-[-0.4px] text-gray-900 md:tracking-[-0.5px] lg:tracking-[-1px]"
			>
				Eliminate delays.<br class="hidden lg:block" />Standardize excellence.
			</h4>
			<p class="font-body text-level-xl w-full font-medium leading-[1.4] tracking-tight text-gray-700">
				Stop wasting time on manual documentation and inconsistent training. Just record a process
				once, and Squint's computer vision turns it into a standard operating procedure available
				to your entire team.
			</p>
		</div>
	</div>
</section>