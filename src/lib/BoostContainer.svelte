<script>
    import Boost from "$lib/Boost.svelte";

    export let data = [];
    export let currentUser = undefined;
    export let who = undefined;
</script>

<div class="flex flex-row gap-2">
    {#each data as item}
        <Boost {who} content={item.content} />
    {/each}
    <Boost
        {who}
        onAdd={(content) => {
            data = [...data, { content: content }];
        }}
    />
</div>
