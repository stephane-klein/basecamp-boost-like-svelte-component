<script>
    import { onMount } from "svelte";

    let element;

    onMount(async () => {
        const { default: Picker } = await import("emoji-picker-element/svelte");
        const picker = new Picker();
        element.appendChild(picker);
        picker.addEventListener("emoji-click", (event) => {
            console.log(event.detail); // will log something like the above
        });
    });
    /*  bind:this={element} */
</script>

<p bind:this={element}>Button</p>
