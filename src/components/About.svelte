
<script>
    let someText = `Flutter developer at Omni`;
    let counter = 0;

    function incrementCounter() {
        counter += 1;
    }
</script>

<style>
    p {
        color: var(--theme-color);
    }    
</style>

<div class="About">
    <p>{ someText }</p>
    <h1>{ counter === 0 ? 'The counter is 0, please increment counter' : counter }</h1>
    <button on:click={ incrementCounter }>Add +1</button>
</div>