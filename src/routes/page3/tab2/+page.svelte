<script>
    import Main from '$lib/components/main.svelte'
    import Nav from '$lib/components/nav.svelte'
    import Footer from '$lib/components/footer.svelte'
    const items = Array(10).fill('Item').map((item, index) => `${item} ${index}`)
</script>

<Nav noTransition>
    <a href="/" slot="start">Home</a>
    <a href="/page2">Page 2</a>
    <a href="#" slot="end" on:click={() => history.back()}>Back</a>
</Nav>
<Main>
    <h1>TAB 2</h1>
    {#each items as item}
        <item>{item}</item>
    {/each}
</Main>
<Footer noTransition>
    <div id="tabs">
        <a href="tab1">Tab1</a>
        <div>Tab2</div>
        <a href="tab3">Tab3</a>
    </div>
</Footer>

<style>
    item {
        background-color: #f007;
        margin: 1px;
        padding: 8px;
        width: 100%;
        text-align: center;
    }
    #tabs {
        width: 100vw;
        display:flex;
        justify-content: space-around;
    }
</style>
