<script>
    let images = [
        {link: 'cpp.png', name: 'C++'},
        {link: 'htmllogo.png', name: 'HMTL'},
        {link: 'CSS3.png', name: 'CSS'},
        {link: 'matlab.png', name: 'Matlab'},
        {link: 'nextjs2.png', name: 'Next.js'},
        {link: 'svelte.png', name: 'Svelte'},
        {link: 'tailwind2.png', name: 'Tailwind'}
    ];
    
    let imageIndex = 0;

    function nextImage() {
        imageIndex = (imageIndex+1) % images.length;
    }
    function prevImage() {
        imageIndex = (imageIndex-1+images.length) % images.length;
    }

</script>

<div class="carousel flex">
    <button class="mr-5 font-extralight text-4xl" on:click={prevImage}>&lt;</button>
    <div class="carousel-images translate-y-6">
        <img src={images[imageIndex].link} alt={`Image ${imageIndex + 1}`} />
        <p class="py-4 text-center text-lg">{images[imageIndex].name}</p>
    </div>
    <button class="ml-5 font-extralight text-4xl" on:click={nextImage}>&gt;</button>
</div>

<style>
    .carousel {
        position: relative;
        max-width: 30%; /* Adjust as needed */
        margin: auto;
    }

    .carousel-images img {
        width: 100%;
        width: 200px;
        height: 200px;
        display: block;
    }
</style>