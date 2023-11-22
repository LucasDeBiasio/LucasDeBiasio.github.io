<script>
    let jobs = [
        {title: 'Job Title', company: 'Company A', duration: 'month 20xx - month 20xx', description: 'Cool Job doing awesome stuff'},
        {title: 'Job Title', company: 'Company B', duration: 'month 20xx - month 20xx', description: 'Cool Job doing awesome stuff'},
        {title: 'Job Title', company: 'Company C', duration: 'month 20xx - month 20xx', description: 'Cool Job doing awesome stuff'},
    ]
</script>

<div class="flex flex-col">
    <div class="mx-40 font-black mt-16 Roboto text-7xl text-center width-100">
        <h1>Experience</h1>
    </div>
    <div class="text-center mt-10 font-light">
        <p>I have no technical work experience so these are just place holders for now</p>
    </div>
    <div class="mb-16 mt-10 mx-40 grid grid-rows-1 gap-y-3">
        {#each jobs as job, index}
        <div class="rounded-lg border border-zinc-400 hover:border-zinc-200 p-5 w-full">
            <div>
                <h1 class="font-semibold text-xl">{job.title}</h1>
                <p class="font-light text-zinc-400">{job.company}, {job.duration}</p>
                <p class="pt-2">{job.description}</p>
            </div>
        </div>
        {/each}
    </div>
</div>
