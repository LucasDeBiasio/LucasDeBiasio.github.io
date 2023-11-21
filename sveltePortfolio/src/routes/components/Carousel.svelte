<script>
    let images = [
        'cpp.png',
        'htmllogo.png',
        'CSS3.png',
        'matlab.png',
        'nextjs2.png',
        'svelte.png',
    ];
    
    let imageIndex = 0;

    function nextImage() {
        imageIndex = (imageIndex+1) % images.length;
    }
    function prevImage() {
        imageIndex = (imageIndex-1+images.length) % images.length;
    }
</script>

<div class="carousel">
    <div class="carousel-images">
        <img src={images[imageIndex]} alt={`Image ${imageIndex + 1}`} />
    </div>
    <button on:click={prevImage}>&lt; Prev</button>
    <button on:click={nextImage}>Next &gt;</button>
</div>

<style>
    .carousel {
        position: relative;
        max-width: 400px; /* Adjust as needed */
        margin: auto;
    }

    .carousel-images img {
        width: 100%;
        display: block;
    }

    button {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        background-color: rgba(0, 0, 0, 0.5);
        color: white;
        border: none;
        cursor: pointer;
        padding: 10px;
    }

    button:first-child {
        left: 10px;
    }

    button:last-child {
        right: 10px;
    }
</style>