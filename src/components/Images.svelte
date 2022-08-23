<script>
    import {isModalOpen, imagen} from '../stores/modalStore'
    import Modal from '../components/Modal.svelte';
    export let data;
    export let imageHeight = 36;
    export let imageSpacing = 0;    
    
</script>

<!--  -->

<div class="flex relative overflow-x-auto w-full">
    <div  class="flex flex-wrap justify-center">
        {#each data as image (image.id)}
            <img  on:click={()=>{imagen.set(image.imgurl);
                    isModalOpen.set(true);
                    console.log("entro desde Images")}} 
                    src={image.imgurl} 
                    alt={image.attribution} 
                    id={image.id} 
                    class={`cursor-pointer w-${imageHeight} mr-${imageSpacing} mb-1`} 
                    />
        {/each}
    </div>
</div>

