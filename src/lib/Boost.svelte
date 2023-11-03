<script>
    let open = false;
    export let who = "";
</script>

{#if open}
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
            />

            <span
                class="cursor-pointer text-green-700"
                on:click={() => {
                    open = false;
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
        <!--
    <svg
        xmlns="http://www.w3.org/2000/svg"
        class="icon icon-tabler icon-tabler-mood-plus"
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
        <path d="M20.985 12.528a9 9 0 1 0 -8.45 8.456"></path>
        <path d="M16 19h6"></path>
        <path d="M19 16v6"></path>
        <path d="M9 10h.01"></path>
        <path d="M15 10h.01"></path>
        <path d="M9.5 15c.658 .64 1.56 1 2.5 1s1.842 -.36 2.5 -1"></path>
    </svg>
    -->
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
