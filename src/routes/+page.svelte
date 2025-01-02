<script>
    import Header from "./header.svelte";
    import Content from "./content.svelte";
    let title = "Web Host";
    let desc = "Dapatkan kebutuhan websitemu hanya di ";
</script>

<Header/>

<br>
    <center>
        <h1>{title}</h1>
        <h3>{desc}{title}!</h3>
    </center>
<br>

<Content/>

<style>

</style>