<script>
    import "../app.css";
    import Header from "./components/Header.svelte";
    
</script>

<div class="relative flex flex-col mx-auto w-full text-sm sm:text-base min-h-screen">
    <Header/>
    <slot />
</div>


  