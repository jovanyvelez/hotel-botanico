<script>
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	const imgUrl = new URL('../lib/assets/wideLeaf.jpeg', import.meta.url).href;
</script>

<div class="mx-40">
	<Navbar let:hidden let:toggle>
		<NavBrand href="/">
			<img src={imgUrl} class="mr-3 h-6 sm:h-9" alt="Flowbite Logo" />
			<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
				Botanico
			</span>
		</NavBrand>
		<NavHamburger on:click={toggle} />
		<NavUl {hidden}>
			<NavLi on:click={toggle} href="/" active={true}>Inicio</NavLi>
			<NavLi on:click={toggle} href="/habitaciones">Habitaciones</NavLi>
			<NavLi
				on:click={toggle}
				href="https://engine.lobbypms.com/botanico-hotel-boutique"
				target="_blank">Reservas</NavLi
			>
			<NavLi href="/pricing">Pricing</NavLi>
			<NavLi href="/contact">Contact</NavLi>
		</NavUl>
	</Navbar>
</div>
