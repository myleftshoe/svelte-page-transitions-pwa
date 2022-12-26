<script>
</script>

<div id="app">
    <slot />
</div>

<style>
    :global(body) {
        box-sizing: border-box;
        margin: 0;
    }
    #app {
        display: grid;
        height: 100vh;
        overflow: hidden;
        grid-template:
            'nav' 3rem
            'main' 1fr
            'footer' 3rem;
    }
</style>
