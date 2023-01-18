<script>
    import { currentLang } from "../stores/store"
    import { LightSwitch } from '@skeletonlabs/skeleton';
    import {mdiWindowClose, mdiWindowMaximize, mdiWindowMinimize, mdiTranslate } from "@mdi/js"
    import IconButton from "../components/IconButton.svelte"
</script>

<div class="p-4 flex justify-between items-center bg-surface-100-800-token select-none" style="--wails-draggable:drag">
    <div class="w-1/3" />
    <h1>Skeleton Wails Template</h1>
    <div class="w-1/3 flex gap-8 justify-end" style="--wails-draggable:no-drag">
        <LightSwitch  />
        <IconButton icon={mdiTranslate} size="20" tooltipText="language" tooltipDirection="bottom" on:click={()=>{$currentLang==="fr" ? $currentLang="en" : $currentLang="fr"}} />
        <div class="flex gap-2">
            <IconButton icon={mdiWindowMinimize} size="20" on:click={()=>{window.runtime.WindowMinimise()}} />
            <IconButton icon={mdiWindowMaximize} size="20" on:click={()=>{window.runtime.WindowToggleMaximise()}} />
            <IconButton icon={mdiWindowClose} size="20" on:click={()=>{window.runtime.Quit()}} />
        </div>
    </div>
</div>