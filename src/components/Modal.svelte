<script>
    import {isModalOpen} from '../stores/modalStore'
</script>

<div class="
            w-screen 
            h-screen 
            fixed           
            top-0 
            left-0 
            flex 
            justify-center 
            items-center
            bg-gray-100
            p-2
            z-10"
            on:click={console.log("desde el maldito div rojo")}>
    <div class="bg-gray-900 text-white rounded-sm px-8 py-10 relative max-w-lg">
        <button  on:click={()=>{isModalOpen.set(false)}} class="absolute top-2 right-3 text-4xl 
            text-gray-300 hover:-translate-y-0.5 
            transition-transform">&times</button>
        <slot />
    </div>
</div>