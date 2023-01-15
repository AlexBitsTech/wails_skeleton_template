<script>
import { LightSwitch } from '@skeletonlabs/skeleton';
import {mdiWindowClose, mdiWindowMaximize, mdiWindowMinimize} from "@mdi/js"
import IconButton from "../components/IconButton.svelte"
</script>

<div class="p-4 flex justify-between items-center bg-surface-100 dark:bg-surface-800 select-none" style="--wails-draggable:drag">
    <div class="w-48" />
    <h1>Skeleton Wails Template</h1>
    <div class="w-48 flex gap-8 justify-end" style="--wails-draggable:no-drag">
        <LightSwitch  />
        <div class="flex gap-2">
            <IconButton icon={mdiWindowMinimize} size="20" on:click={()=>{window.runtime.WindowMinimise()}} />
            <IconButton icon={mdiWindowMaximize} size="20" on:click={()=>{window.runtime.WindowToggleMaximise()}} />
            <IconButton icon={mdiWindowClose} size="20" on:click={()=>{window.runtime.Quit()}} />
        </div>
    </div>
</div>