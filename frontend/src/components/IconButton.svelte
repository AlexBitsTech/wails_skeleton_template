<script lang="ts">
    import SvgIcon from "@jamescoyle/svelte-icon"
    import { tooltip } from '@skeletonlabs/skeleton';
    
    export let icon:string
    export let size:string = "24"
    export let tooltipText = ""
    export let tooltipDirection = "top"
</script>

{#if tooltipText}
<div use:tooltip={{content:tooltipText, position: tooltipDirection}} on:click class="hover:text-primary-500 active:text-primary-700">
    <SvgIcon type="mdi" path={icon} {size} />
</div>
{:else}
<div on:click class="hover:text-primary-500 active:text-primary-700">
    <SvgIcon type="mdi" path={icon} {size} />
</div>
{/if}