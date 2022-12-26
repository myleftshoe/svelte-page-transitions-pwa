<script>
    import { fly } from 'svelte/transition'
</script>

<footer>
    <div>
        <slot />
    </div>
</footer>

<style>
    footer {
        grid-area: footer;
        display: grid;
        place-content: center;
        background-color: pink;
    }
</style>
