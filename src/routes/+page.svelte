<script lang="ts">
	import Navbar from '../components/Navbar.svelte';
	import bg from '$lib/assets/webaliser-_TPTXZd9mOo-unsplash.jpg';
	import { ArrowRightOutline, HomeSolid } from 'flowbite-svelte-icons';
	import intro from '$lib/assets/olimpia-campean-zkLOBGkthJo-unsplash.jpg';
	import SectionHead from '../components/SectionHead.svelte';
	let btnHover = false;
	const handleBtnHover = () => {
		btnHover = true;
	};
	const handleBtnHoverOut = () => {
		btnHover = false;
	};
</script>

<section id="hero" class="relative min-h-screen">
	<Navbar />
	<!-- Background -->
	<div
		class={` h-full absolute top-0 bottom-0 right-0 left-0 -z-10  after:absolute after:top-0 after:bottom-0 after:left-0 after:right-0 after:bg-gradient-to-tl after:from-black after:to-transparent`}
	>
		<img src={bg} alt="bg" class="object-cover w-full h-full" />
	</div>
	<!-- Your website content here -->
	<div class="flex flex-col gap-8 mx-3 md:mx-28 mt-20 sm:mx-12">
		<div
			class="flex bg-gradient-to-l from-red-300 w-fit text-xl font-light text-blue-800 items-center p-2 tracking-[0.4em] lines gap-2"
		>
			<HomeSolid size={'xl'} />
			REAL ESTATE AGENCY
		</div>

		<div class="space-y-3 text-white">
			<h1 class="text-6xl font-bold text-white">Find Your Perfect Home</h1>
			<p>
				Our highly educated staff will make sure that your project will be finished on time and
				specified budget.
			</p>

			<button
				on:mouseover={handleBtnHover}
				on:focus={handleBtnHover}
				on:mouseleave={handleBtnHoverOut}
				class="flex items-center gap-5 px-10 py-6 text-xl text-blue-900 bg-white rounded-md w-fit"
			>
				<span> Explore Property </span>
				<div class={`w-fit ${btnHover ? 'translate-x-2' : null} rounded-full bg-yellow-300 p-1`}>
					<ArrowRightOutline />
				</div>
			</button>
		</div>
	</div>
</section>
<!-- introduction -->
<section id="intro" class="min-h-screen px-4 md:px-28 py-10 leading-loose">
	<SectionHead
		head={{
			no: 1,
			section_title: 'Properland intro',
			title: 'A Property Management Company You Can Trust'
		}}
	/>
	<div class="md:flex">
		<div class="px-4 mt-5 text-red-500 flex-grow md:text-xl">
			<p>
				We focus on the importance of dignity and respect in the provision of our care to property
				owners, tenants, and the investment properties our renters call home. All our efforts are
				concentrated on stewardship and compassionate tenant ministration. Situated at the epicenter
				of Silicon Valley, we possess cutting-edge technology to address the comprehensive
				requirements of investment properties, property owners and residents alike.
			</p>
		</div>
		<div class="mt-10 md:mt-5 overflow-hidden rounded-lg w-[250em]">
			<img src={intro} class="object-cover w-full h-full" alt="introduction " />
		</div>
	</div>
</section>

<!-- properties -->
<section id="properties" class="h-screen px-4 md:px-28 py-10 leading-loose bg-gray-300">
	<SectionHead
		head={{
			no: 2,
			section_title: 'properties',
			title: 'Properties for sale in your favorite area'
		}}
	/>
</section>
