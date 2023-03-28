<script>
    import Button from "./Button.svelte";
    let someText = `Flutter developer at Omni`;
    let counter = 0;
    let styles = { isDark: false };

    function incrementCounter() {
        counter += 1;
    }

    function toggleDarkMode() {
        styles.isDark = !styles.isDark;
        window.document.body.classList.toggle("dark-theme");
    }

</script>

<style>
    p {
        color: var(--theme-color);
    }    
</style>

<div class="About">
    <p>{ someText }</p>

    { #if !styles.isDark }
        <p>Light theme selected</p>
    { :else }
        <p>Dark theme selected</p>
    { /if }

    <h1>{ counter === 0 ? 'The counter is 0, please increment counter' : counter }</h1>
    <Button 
        text="Increment" 
        counter={ counter } 
        on:click={ incrementCounter }    
    />
</div>