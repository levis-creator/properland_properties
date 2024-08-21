<script lang="ts">
	import type { MenuItem } from '$lib/types.js';
	import { NavLi, NavUl } from 'flowbite-svelte';
	export let menuitems: MenuItem[];
	export let isOpen;
</script>

<NavUl
	hidden={isOpen}
	ulClass="text-xl flex flex-col border-none gap-5 bg-white mt-5 md:flex-row md:items-center"
>
	{#each menuitems as menu}
		<NavLi nonActiveClass={'text-gray-300 hover:text-blue-900 '} href={menu.route}
			>{menu.title}</NavLi
		>
	{/each}
	<buttons class="hidden rounded-md md:inline-block bg-blue-900 px-10 py-5 text-white w-fit">
		Contact</buttons
	>
</NavUl>
