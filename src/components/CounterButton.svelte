<script>
    import { counter } from '../store/store.js';
    function handleClick() {
        counter.update( n => n + 1 );
    }
</script>

<style>
    button {
        background-color: #f76027;
        color: white;
        border: none;
        border-radius: 8px;
        padding: 0.5rem;
        text-transform: uppercase;
        cursor: pointer;
    }
</style>

<button on:click={ handleClick } >
    Click { $counter === 0 ? '' : $counter }
</button>