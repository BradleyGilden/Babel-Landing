<script>
    import Navbar from "./components/Navbar.svelte";
    import Quotes from "./components/Quotes.svelte";
    import About from "./components/About.svelte";
    import Guide from "./components/Guide.svelte";
    import { gsap } from "gsap";

    import { ScrollTrigger } from "gsap/ScrollTrigger";
    import { ScrollToPlugin } from "gsap/ScrollToPlugin";

    gsap.registerPlugin(ScrollTrigger, ScrollToPlugin);
</script>

<main class="">
    <Guide />
    <div class="flex flex-col relative h-screen">
        <img
            class="absolute object-center object-cover h-full w-full opacity-40"
            src="https://i.ibb.co/NtqJqkT/communication.jpg"
            alt="hero"
        />
        <Navbar />
        <Quotes />
    </div>
    <div class="h-screen flex gap-5">
        <About />
    </div>
</main>

<style>
</style>
