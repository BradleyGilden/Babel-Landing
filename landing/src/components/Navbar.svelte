<script>
    import ThemeSelect from "./ThemeSelect.svelte";
    import gsap from "gsap";

</script>
<div id="navbar" class="relative navbar bg-[rgb(15,23,42,0.8)] rounded-3xl shadow-base-300 shadow-lg z-10">
    <svg
        class="h-10 text-primary ml-2"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        fill="currentColor"
        ><path
            d="M10 3H14C18.4183 3 22 6.58172 22 11C22 15.4183 18.4183 19 14 19V22.5C9 20.5 2 17.5 2 11C2 6.58172 5.58172 3 10 3Z"
        ></path></svg
    >
    <!-- svelte-ignore a11y-missing-attribute -->
    <a
        aria-label="header"
        href={window.location.href}
        class="btn btn-ghost text-3xl">Babel Chat</a
    >

    <div class="absolute flex gap-10 mx-auto left-1/2 translate-x-[-50%]">
        <button
            class="hover:btn hover:bg-base-300 rounded-3xl transition-all"
            on:click={() => {gsap.to(window, { duration: 1, scrollTo: '#about' })}}
            >About</button
        >
        <button
            class="hover:btn hover:bg-base-300 rounded-3xl transition-all"
            on:click={() => {gsap.to(window, { duration: 1, scrollTo: '#features' })}}
            >Features</button
        >
        <a
            target="_blank"
            rel="noopener noreferrer"
            href="https://comascript.hashnode.dev"
            class="hover:btn hover:bg-base-300 rounded-3xl transition-all"
            >Blog
        </a>
        <button
            class="hover:btn hover:bg-base-300 rounded-3xl transition-all"
            on:click={() => {gsap.to(window, { duration: 1, scrollTo: '#qr-code' })}}
            >Pricing</button
        >
        <a
            target="_blank"
            rel="noopener noreferrer"
            href="https://www.linkedin.com/in/bradley-gilden"
            class="hover:btn hover:bg-base-300 rounded-3xl transition-all"
            >Contact
        </a>
    </div>

    <div class="absolute right-5 flex gap-5">
        <ThemeSelect size={'10'} />
        <a 
            class="btn btn-primary rounded-3xl text-xl"
            href="https://chat.bradleygilden.tech"
            target="_blank"
            rel="noopener noreferrer"
        >Signup</a>
    </div>
</div>
