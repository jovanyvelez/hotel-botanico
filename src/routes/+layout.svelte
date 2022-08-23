<script>
	import '../app.postcss';
	import Navbar from '../components/Navbar.svelte';
	import {isModalOpen, imagen} from '../stores/modalStore'
    import Modal from '../components/Modal.svelte';
</script>

	<Navbar />
	<slot />
	{#if $isModalOpen}
		<Modal>
			<img src={$imagen} alt="nada">
		</Modal>
	{/if} 	

