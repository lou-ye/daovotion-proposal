<script>
    import Icon from "./Icon.svelte";
    import NavBar from "./NavBar.svelte";
    import Language from "./Language.svelte";
    import Profile from "./Profile.svelte";
</script>

<style>
    .Header-content {
        padding: 10px;
        display: flex;
        align-items: center;
        font-size: 1.3rem;
    }
</style>

<div class="Header">
    <header class="Header-content">
        <Icon />
        <NavBar />
        <Language />
        <Profile />
    </header>
</div>