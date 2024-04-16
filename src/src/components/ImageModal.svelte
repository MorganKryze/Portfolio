<script>
    let showModal = true;
    export let image;
</script>

<div class="relative">
    <button class="focus:outline-none focus:ring-2 focus:ring-blue-500" on:click={() => { showModal = true; console.log(showModal); }}>
        <img
            src={image}
            alt="gallery"
            class="w-full object-cover rounded-md"
        />
    </button>
    {#if showModal}
        <div class="absolute inset-0 flex items-center justify-center bg-black bg-opacity-50">
            <div class="bg-white p-4 rounded-md">
                <img src={image} alt="gallery" class="w-full object-cover rounded-md" />
                <button class="mt-4 px-2 py-1 bg-red-500 text-white rounded-md" on:click={() => (showModal = false)}>Close</button>
            </div>
        </div>
    {/if}
</div>