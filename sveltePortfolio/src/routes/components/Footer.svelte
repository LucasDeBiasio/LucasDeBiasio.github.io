<script>
    let socials = [
        {name: 'linkedIn', link: '', icon: 'fa-brands fa-linkedin'},
        {name: 'github', link: 'https://github.com/LucasDeBiasio', icon: 'fa-brands fa-github'},
        {name: 'email', link: '', icon: 'fa-solid fa-at'},
    ]
</script>

<footer class="py-2 sticky top-[100vh] w-full font-light Roboto sm:flex items-center gap-4 hidden justify-around border border-amber-50 border-b-0 border-l-0 border-r-0 border-t-1">
    {#each socials as social, index}
        <div class="duration-200 px-2 rounded-lg hover:bg-slate-700">
            <a class="flex flex-row items-center" target = "blank" href={social.link}>
                <i class="{social.icon} px-1"></i>
                <p>{social.name}</p>
            </a>
        </div>
    {/each}
    </footer>