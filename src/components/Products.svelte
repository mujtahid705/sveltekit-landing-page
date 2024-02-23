<script>
	import ProductCard from "./ProductCard.svelte";
	import SectionWrapper from "./SectionWrapper.svelte";
	let productFeatures = [
		{
			featureList: ["Custom size shirts", "Premium fabric", "Made for your own body"],
			description:
				"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pharetra molestie convallis. Vestibulum felis elit, laoreet ut felis convallis, euismod hendrerit lacus. ",
			imageUrl:
				"https://images.pexels.com/photos/1926769/pexels-photo-1926769.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
		},
		{
			featureList: ["Custom size shirts", "Premium fabric", "Made for your own body"],
			description:
				"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pharetra molestie convallis. Vestibulum felis elit, laoreet ut felis convallis, euismod hendrerit lacus. ",
			imageUrl:
				"https://images.pexels.com/photos/322207/pexels-photo-322207.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
		},
		{
			featureList: ["Custom size shirts", "Premium fabric", "Made for your own body"],
			description:
				"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pharetra molestie convallis. Vestibulum felis elit, laoreet ut felis convallis, euismod hendrerit lacus. ",
			imageUrl:
				"https://images.pexels.com/photos/1183266/pexels-photo-1183266.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
		}
	];
</script>

<SectionWrapper id="projects">
	<div
		class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
	>
		<div class="flex flex-xol gap-2">
			<p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
				Start your
				<span class="text-indigo-400">fashion hunting</span>
				today
			</p>
			<h3
				class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] max-auto w-full font-semibold text-center"
			>
				Fashion For Everyone
			</h3>
		</div>

		{#each productFeatures as productFeature, i}
			<ProductCard index={i} {productFeature}>
				{#if i === 0}
					Get clothes
					<span class="text-indigo-400 font-medium"> specially made </span>
					for you
				{:else if i === 1}
					Get
					<span class="text-indigo-400 font-medium">premium</span>
					product
				{:else}
					Lorem ipsum dolor sit
					<span class="text-indigo-400 font-medium"> amet, consectetur adipiscinge </span>
					elit.
				{/if}
			</ProductCard>
		{/each}
	</div>
</SectionWrapper>
