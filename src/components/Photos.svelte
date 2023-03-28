<script>
    import { onMount } from "svelte";
    let photos = [];
    
    onMount(async () => {
        const response = await fetch('https://rickandmortyapi.com/api/character?_limit=40');
        const jsonResponse = await response.json();
        photos = jsonResponse.results;
    });

</script>

<style>
    .Photos {
        width: 100%;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-gap: 8px;
    }
</style>

<div class="Photos">
    { #each photos as { name, image } }
        <figure>
            <img src={ image } alt={name} >
            <figcaption>{ name }</figcaption>
        </figure>
    { :else }
        <p>Loading...</p>
    { /each }
</div>