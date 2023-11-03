<script>
    import Boost from "$lib/Boost.svelte";

    export let data = [];
    export let currentUser = undefined;
    export let who = undefined;
</script>

<div class="flex flex-row gap-2">
    {#each data as item, i}
        <Boost
            {who}
            content={item.content}
            onRemove={() => {
                data = data.filter((_, index) => index != i);
            }}
        />
    {/each}
    <Boost
        {who}
        onAdd={(content) => {
            data = [...data, { content: content }];
        }}
    />
</div>
