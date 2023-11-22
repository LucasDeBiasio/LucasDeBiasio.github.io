<script>
    let tabs = [
        {name: 'Projects', link: '/projects'},
        {name: 'Experience', link: '/experience'},
        {name: 'Resume', link: '/resume'},
    ];
</script>

<header class="sticky px-4 py-2 flex items-center justify-between border border-amber-50 border-b-1 border-l-0 border-r-0 border-t-0">
    <a href="/" class="flex flex-row duration-200 px-2 hover:bg-neutral-700">
        <h1 class="font-medium text-lg Roboto">&lt &#x2f &gt Lucas <span class="uppercase"> De Biasio</span></h1>
    </a>
    <div class="font-light Roboto sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <div class="duration-200 px-2 hover:bg-neutral-700">
                <a href={tab.link}>
                    <p>{tab.name}</p>
                </a>
            </div>
        {/each}
    </div>
</header>