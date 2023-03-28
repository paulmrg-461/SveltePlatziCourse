<script>
    export let name = 'name';
    export let value = '';

</script>

<div class="Input">
    <input 
        type="text" 
        name={ name } 
        bind:value={ value }
    >
    <p>Hello { value }</p>
</div>