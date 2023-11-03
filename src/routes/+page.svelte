<script>
    import Boost from "$lib/Boost.svelte";
</script>

<div class="flex flex-col gap-4 w-2/3 mx-auto py-8">
    <div class="flex flex-row gap-2">
        <img
            class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
            src="https://images.unsplash.com/photo-1491528323818-fdd1faba62cc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
            alt=""
        />
        <div class="flex flex-col gap-2">
            <span class="font-semibold">John Doe</span>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris ullamcorper, odio lobortis vestibulum
                fermentum, nibh nisi scelerisque nibh, elementum varius leo nulla a ligula. Phasellus sed arcu placerat,
                blandit diam in, congue metus. Proin molestie lectus quis orci faucibus, non egestas risus convallis.
            </p>
            <Boost who="John" />
        </div>
    </div>

    <div class="border-t pt-4">
        <div class="flex flex-row gap-2">
            <img
                class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
                src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                alt=""
            />
            <div class="flex flex-col gap-2">
                <span class="font-semibold">Alice Doe</span>
                <p>
                    Morbi semper non lorem sit amet ullamcorper. Quisque dapibus tortor sed orci fermentum, sit amet
                    dapibus justo malesuada. Fusce imperdiet purus augue, ut suscipit quam elementum et. Fusce sit amet
                    dictum augue. Integer imperdiet eros tincidunt vulputate tempor.
                </p>
                <Boost who="Alice" />
            </div>
        </div>
    </div>

    <div class="border-t pt-4">
        <div class="flex flex-row gap-2">
            <img
                class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
                src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                alt=""
            />
            <div class="flex flex-col gap-2">
                <span class="font-semibold">Alice Doe</span>
                <p>
                    Morbi lobortis, tortor nec interdum consequat, nunc urna venenatis sapien, vel auctor lectus justo
                    id sapien. Quisque ultrices vulputate commodo. Aliquam erat volutpat. Phasellus hendrerit ligula
                    vitae dignissim imperdiet. Phasellus nibh dolor, commodo vel laoreet et, porttitor vitae odio.
                </p>
                <Boost who="Alice" />
            </div>
        </div>
    </div>
</div>
