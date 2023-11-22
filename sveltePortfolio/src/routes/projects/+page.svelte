<script>
    let projects = [
        {name: 'Svelte Portfolio', link: 'https://github.com/LucasDeBiasio/sveltePortfolio', description: 'Minimal personal portfolio website made using SvelteKit and Tailwind. Emulated the style of Vercels company website. Created this website as an assignment in one of my school classes, CMPT 276. After the semester ends, I will be updating it to make it even better', techs: 'Svelte, Tailwind'},
        {name: 'Empty', link: '', description: 'No project yet', techs: 'n/a'},
        {name: 'Empty', link: '', description: 'No project yet', techs: 'n/a'},
    ];
</script>
<div class="flex flex-col ">
    <div class="mx-40 font-black mt-16 Roboto text-7xl text-center width-100">
        <h1>Projects</h1>
    </div>
    <div class="mt-16 mx-24 grid grid-cols-3 gap-x-5 justify-items-center">
        {#each projects as project, index}
        <div class="rounded-lg border border-zinc-400 hover:border-zinc-200 p-5 w-full">
            <div class="flex justify-between">
                <h1 class=" font-semibold text-xl">{project.name}</h1>
                <div class="px-1 rounded-md border border-zinc-400 hover:border-zinc-200">
                    <a target="_blank" href={project.link}><i class="fas fa-link"></i></a>
                </div>
            </div>
            <p class="my-5 font-light h-2/3 py-5 border-y border-zinc-500">{project.description}</p>
            <p class="font-light">Stack: {project.techs}</p>
        </div>
        {/each}
    </div>
</div>
