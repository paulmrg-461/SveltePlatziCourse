<script>
    export let counter = 0;
    export let text;
</script>

<button on:click>
    { text }
    { counter === 0 ? '' : counter }
</button>