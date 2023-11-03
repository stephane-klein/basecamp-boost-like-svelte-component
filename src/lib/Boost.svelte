<script>
    let open = false;
    export let who = "";
    export let content = undefined;
    export let onAdd = undefined;
    export let onRemove = undefined;
    let edit_content = "";
</script>

{#if content}
    <div class="flex flex-row bg-gray-200 rounded-full p-0 items-center pr-2">
        <img
            class="inline-block h-6 w-6 rounded-full"
            src="https://images.unsplash.com/photo-1491528323818-fdd1faba62cc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
            alt=""
        />
        <span
            class="px-2 py-1 cursor-pointer"
            on:click={() => {
                open = true;
            }}
        >
            {content}
        </span>
        {#if open}
            <span
                class="cursor-pointer text-red-600"
                on:click={() => {
                    if (onRemove) {
                        onRemove();
                    }
                }}
            >
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="icon icon-tabler icon-tabler-trash"
                    width="20"
                    height="20"
                    viewBox="0 0 24 24"
                    stroke-width="2"
                    stroke="currentColor"
                    fill="none"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                >
                    <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                    <path d="M4 7l16 0"></path>
                    <path d="M10 11l0 6"></path>
                    <path d="M14 11l0 6"></path>
                    <path d="M5 7l1 12a2 2 0 0 0 2 2h8a2 2 0 0 0 2 -2l1 -12"></path>
                    <path d="M9 7v-3a1 1 0 0 1 1 -1h4a1 1 0 0 1 1 1v3"></path>
                </svg>
            </span>
        {/if}
    </div>
{:else if open}
    <div class="flex flex-row">
        <div class="flex flex-row bg-gray-200 rounded-full py-1 px-2 items-center">
            <img
                class="inline-block h-6 w-6 rounded-full ring-2 ring-gray-300"
                src="https://images.unsplash.com/photo-1491528323818-fdd1faba62cc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                alt=""
            />
            <input
                type="text"
                maxlength="16"
                class="w-40 px-2 py-1 bg-transparent focus:outline-none"
                autofocus="autofocus"
                placeholder={`Boost ${who}`}
                bind:value={edit_content}
            />

            <span
                class="cursor-pointer text-green-700"
                on:click={() => {
                    open = false;
                    if (onAdd) {
                        onAdd(edit_content);
                    }
                    edit_content = "";
                }}
            >
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="icon icon-tabler icon-tabler-circle-check"
                    width="24"
                    height="24"
                    viewBox="0 0 24 24"
                    stroke-width="2"
                    stroke="currentColor"
                    fill="none"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                >
                    <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                    <path d="M12 12m-9 0a9 9 0 1 0 18 0a9 9 0 1 0 -18 0"></path>
                    <path d="M9 12l2 2l4 -4"></path>
                </svg>
            </span>
            <span
                class="cursor-pointer text-red-600"
                on:click={() => {
                    open = false;
                    edit_content = "";
                }}
            >
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="icon icon-tabler icon-tabler-circle-x"
                    width="24"
                    height="24"
                    viewBox="0 0 24 24"
                    stroke-width="2"
                    stroke="currentColor"
                    fill="none"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                >
                    <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                    <path d="M12 12m-9 0a9 9 0 1 0 18 0a9 9 0 1 0 -18 0"></path>
                    <path d="M10 10l4 4m0 -4l-4 4"></path>
                </svg>
            </span>
        </div>
    </div>
{:else}
    <div
        class="bg-gray-200 rounded-full flex flex-row px-2 py-1 justify-center inline-block w-fit cursor-pointer"
        on:click={() => {
            open = true;
        }}
    >
        <svg
            xmlns="http://www.w3.org/2000/svg"
            class="icon icon-tabler icon-tabler-message-circle-plus"
            width="20"
            height="20"
            viewBox="0 0 24 24"
            stroke-width="2"
            stroke="currentColor"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
        >
            <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
            <path
                d="M12.007 19.98a9.869 9.869 0 0 1 -4.307 -.98l-4.7 1l1.3 -3.9c-2.324 -3.437 -1.426 -7.872 2.1 -10.374c3.526 -2.501 8.59 -2.296 11.845 .48c1.992 1.7 2.93 4.04 2.747 6.34"
            ></path>
            <path d="M16 19h6"></path>
            <path d="M19 16v6"></path>
        </svg>
    </div>
{/if}
