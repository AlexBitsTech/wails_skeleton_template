<script lang="ts">
    import SvgIcon from "@jamescoyle/svelte-icon"
    
    export let icon:string
    export let size:string = "24"
</script>

<div on:click class="hover:text-primary-500 active:text-primary-700">
    <SvgIcon type="mdi" path={icon} {size} />
</div>