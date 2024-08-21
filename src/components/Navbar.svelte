<script lang="ts">
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	import logo from '$lib/assets/property.svg';
	import { menuitems } from '$lib/data/menuitem.js';
	import NavItem from './NavItem.svelte';
	let isOpen = true;
	function toggleMenu() {
		isOpen = !isOpen;
	}
</script>

<Navbar let:NavContainer color="primary">
	<NavContainer class="p-5 border mt-8 rounded-lg bg-white ">
		<NavBrand href="/">
			<img src={logo} class="me-3 h-11 lg:h-20" alt="Flowbite Logo" />
		</NavBrand>
		<NavHamburger
			menuClass={`${!isOpen ? 'bg-yellow-300' : 'bg-blue-900'}  text-white w-12 h-12 p-2`}
			onClick={() => toggleMenu()}
		/>
		<NavItem {menuitems} {isOpen} />
	</NavContainer>
</Navbar>
