<script>
	import {images} from '../../stores/modalStore'
	import Images from '../../components/Images.svelte';
	//import images from '../../data';
	let data = [...$images];

	const shuffle = (data) => {
		for (let i = data.length - 1; i > 0; i--) {
			const j = Math.floor(Math.random() * (i + 1));
			const temp = data[i];

			// Swap
			data[i] = data[j];
			data[j] = temp;
		}
		return data;
	};
	$: tmp = shuffle(data);
</script>



<div>
    <h1 class="text-center text-5xl bg-teal-200 my-4 text-slate-700 p-4">Porque sabemos lo que amas te damos lo mejor</h1>
</div>

<main  class="w-screen mx-2">
	<div on:click={console.log("Desde main")}>
		<Images {data} imageHeight={36} imageSpacing={1} />
	</div>
</main>
