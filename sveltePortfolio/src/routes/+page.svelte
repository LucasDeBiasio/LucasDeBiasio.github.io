<script>
    import Carousel from "./components/Carousel.svelte";

    let name = 'world';
    console.log(name);

    let socials = [
        {name: 'linkedIn', link: 'https://www.linkedin.com/in/lucasdebiasio/', icon: 'fa-brands fa-linkedin'},
        {name: 'github', link: 'https://github.com/LucasDeBiasio', icon: 'fa-brands fa-github'},
        {name: 'email', link: 'mailto:lucasnoeldeb@gmail.com', icon: 'fa-solid fa-at'},
    ]
    
</script>

<div class="absolute top-[40vh] h-[50vh]">
    <div class="mx-40 gap-10 flex">
        <div class="w-4/6">
            <h1 class="font-black text-7xl Roboto">Lucas <span class="uppercase"> De Biasio</span>,</h1>
            <p class="text-xl font-light py-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer consectetur, turpis at placerat cursus, enim neque blandit dui, sit amet aliquet ex lectus sit amet lorem. Quisque sagittis risus quis dictum interdum. Fusce eget erat hendrerit ex egestas auctor et vitae est. Praesent sed ullamcorper erat, sed tempor justo.</p>
            <div class="font-light Roboto sm:flex items-center">
                {#each socials as social, index}
                    <div class="duration-200 px-2 rounded-lg hover:bg-slate-700">
                        <a id="mod" class="flex flex-row items-center" target = "blank" href={social.link}>
                            <i class="{social.icon} px-1"></i>
                            <p>{social.name}</p>
                        </a>
                    </div>
                {/each}
                </div>
        </div>
        <Carousel></Carousel>
    </div>
</div>

