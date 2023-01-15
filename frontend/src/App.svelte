<script>
    import {AppShell} from "@skeletonlabs/skeleton"
    import Header from "./components/Header.svelte"
    import Footer from "./components/Footer.svelte"
    import PageMain from "./pages/PageMain.svelte"
</script>

<AppShell class="min-h-screen">
	<svelte:fragment slot="header"><Header /></svelte:fragment>
	<PageMain />
	<svelte:fragment slot="footer"><Footer /></svelte:fragment>
</AppShell>


