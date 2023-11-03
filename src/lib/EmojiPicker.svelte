<script>
    import { Popover, PopoverButton, PopoverPanel } from "@rgossiaux/svelte-headlessui";

    export let onSelect = undefined;
    let element;
</script>

<Popover style="position: relative;" let:open let:close>
    <PopoverButton
        on:click={async () => {
            if (!open) {
                const { default: Picker } = await import("emoji-picker-element/svelte");
                const picker = new Picker();
                element.appendChild(picker);
                picker.addEventListener("emoji-click", (event) => {
                    if (onSelect) {
                        onSelect(event.detail);
                    }
                    close();
                });
            }
        }}
    >
        Open
    </PopoverButton>

    <PopoverPanel style="position: absolute; z-index: 10;">
        <div bind:this={element}></div>
    </PopoverPanel>
</Popover>
