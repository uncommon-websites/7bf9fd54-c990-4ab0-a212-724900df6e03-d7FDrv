<script lang="ts">
	// Props
	let { className = '' }: { className?: string } = $props();
</script>

<section class="container {className}">
	<div class="bg-[var(--color-background)] py-16 sm:py-24 lg:py-32">
		<div class="mx-auto max-w-7xl rounded-[40px] bg-primary-50 p-8 lg:p-20">
			<div class="flex flex-col gap-10 lg:flex-row lg:gap-20">
				<div class="flex flex-1 flex-col justify-center gap-6 lg:gap-10">
					<div class="flex flex-col gap-6">
						<h2
							class="font-display text-level-5xl font-semibold leading-tight tracking-tighter text-gray-900"
						>
							Transform video into searchable, step-by-step guides.
						</h2>
						<div
							class="font-body space-y-5 text-level-xl font-medium leading-relaxed text-gray-700"
						>
							<p>
								Squint's AI analyzes your captured video, automatically generating step-by-step work
								instructions with annotated screenshots and clear descriptions.
							</p>
							<p>
								Turn hours of video into a searchable knowledge base that anyone can follow, ensuring
								procedures are always up-to-date and accessible right on the factory floor.
							</p>
						</div>
					</div>
					<div class="flex flex-col items-start gap-2 sm:flex-row sm:items-center sm:gap-4">
						<a
							href="#"
							class="font-body flex h-12 w-full items-center justify-center gap-4 rounded-2xl bg-primary-600 px-6 text-level-xl font-medium text-white shadow-sm transition hover:bg-primary-700 sm:w-auto lg:h-16"
						>
							<span>Explore Features</span>
							<span>→</span>
						</a>
						<a
							href="#"
							class="font-body flex h-12 w-full items-center justify-center gap-4 rounded-2xl px-6 text-level-xl font-medium text-primary-600 transition hover:bg-primary-100 sm:w-auto lg:h-16"
						>
							<span>Get Started Free</span>
							<span>→</span>
						</a>
					</div>
				</div>
				<div class="relative flex-1">
					<img
						src="https://www.ledr.com/colours/black.jpg"
						alt="A generated step-by-step guide for a manufacturing process shown on a tablet."
						class="h-full w-full rounded-3xl object-cover lg:aspect-[1.04]"
					/>
					<div
						class="absolute bottom-4 left-4 flex items-center gap-2 rounded-2xl bg-white p-3 shadow-sm lg:p-4"
					>
						<div class="flex h-4 w-4 items-center justify-center">
							<svg
								viewBox="0 0 16 16"
								fill="none"
								class="h-full w-full text-primary-500"
								aria-hidden="true"
							>
								<path
									d="M2.75 8.75L6.25 12.25L13.25 4.75"
									stroke="currentColor"
									stroke-width="2"
									stroke-linecap="round"
									stroke-linejoin="round"
								></path>
							</svg>
						</div>
						<p class="font-body text-level-lg font-medium text-primary-600">
							Process Standardized
						</p>
					</div>
				</div>
			</div>
			<div class="mt-10 border-t border-gray-200 lg:mt-20">
				<div class="flex flex-col lg:flex-row">
					<div class="flex-1 py-10 lg:py-20 lg:pr-10 xl:pr-20">
						<div class="flex flex-col gap-6">
							<img
								src="https://www.ledr.com/colours/black.jpg"
								alt="An example of a visual instruction with annotations and highlights."
								class="aspect-video w-full rounded-2xl object-cover"
							/>
							<div class="flex flex-col gap-2 lg:gap-4">
								<h4
									class="font-display text-level-3xl font-semibold leading-tight tracking-tight text-gray-800"
								>
									Visual instructions that leave no room for error.
								</h4>
								<div
									class="font-body space-y-5 text-level-xl font-medium leading-relaxed text-gray-700"
								>
									<p>
										Squint doesn't just record video. It breaks down every action into a clear,
										visual step with automatic annotations.
									</p>
									<p>
										Ensure every team member performs tasks correctly and consistently, reducing
										defects, rework, and safety incidents.
									</p>
								</div>
							</div>
						</div>
					</div>
					<div class="my-8 h-px w-full bg-gray-200 lg:my-0 lg:h-auto lg:w-px"></div>
					<div class="flex-1 py-10 lg:py-20 lg:pl-10 xl:pl-20">
						<div class="flex flex-col gap-6">
							<img
								src="https://www.ledr.com/colours/black.jpg"
								alt="A searchable library of work instructions on a computer screen."
								class="aspect-video w-full rounded-2xl object-cover"
							/>
							<div class="flex flex-col gap-2 lg:gap-4">
								<h4
									class="font-display text-level-3xl font-semibold leading-tight tracking-tight text-gray-800"
								>
									A living library of your team's expertise.
								</h4>
								<div
									class="font-body space-y-5 text-level-xl font-medium leading-relaxed text-gray-700"
								>
									<p>
										Build a searchable database of all your critical processes. New hires can
										self-train, and experienced workers can quickly reference best practices.
									</p>
									<p>
										Minimize interruptions and costly production delays by giving everyone instant
										access to the knowledge they need, when they need it.
									</p>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>