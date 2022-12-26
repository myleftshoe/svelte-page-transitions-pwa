<script>
    import { fly, scale } from 'svelte/transition'
</script>

<main in:fly={{ x: 375, opacity: 1 }} out:fly={{ x: -375, opacity: 1 }} >
    <slot />
</main>

<style>
    main {
        grid-area: main;
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: #0f07;
    }
</style>
