<script>
    let name = 'world';
    console.log(name);

    let socials = [
        {name: 'linkedIn', link: 'https://www.linkedin.com/in/lucasdebiasio/', icon: 'fa-brands fa-linkedin'},
        {name: 'github', link: 'https://github.com/LucasDeBiasio', icon: 'fa-brands fa-github'},
        {name: 'email', link: 'mailto:lucasnoeldeb@gmail.com', icon: 'fa-solid fa-at'},
    ]
    
</script>

<div class="bg-red-500 flex items-center h-[95.3vh]">
    <div class="flex">
        <div class="bg-green-500 w-4/6">
            <h1 class="font-black text-6xl Roboto">Lucas <span class="uppercase"> De Biasio</span>,</h1>
            <p class="text-lg font-light py-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer consectetur, turpis at placerat cursus, enim neque blandit dui, sit amet aliquet ex lectus sit amet lorem. Quisque sagittis risus quis dictum interdum. Fusce eget erat hendrerit ex egestas auctor et vitae est. Praesent sed ullamcorper erat, sed tempor justo.</p>
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
        <div class="bg-blue-500 w-2/6">
            <h1>hi</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer consectetur, turpis at placerat cursus, enim neque blandit dui, sit amet aliquet ex lectus sit amet lorem. Quisque sagittis risus quis dictum interdum. Fusce eget erat hendrerit ex egestas auctor et vitae est. Praesent sed ullamcorper erat, sed tempor justo. Sed hendrerit ante at diam placerat, vitae fermentum lectus aliquet. Nulla ac nibh ut justo cursus molestie nec eget justo. Nulla sollicitudin ultrices erat a tempus. Morbi egestas semper nulla congue facilisis.</p>
        </div>
    </div>
</div>

