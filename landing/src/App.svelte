<script>
    import Navbar from "./components/Navbar.svelte";
    import Quotes from "./components/Quotes.svelte";
    import About from "./components/About.svelte";
    import Guide from "./components/Guide.svelte";
    import Pricing from "./components/Pricing.svelte";
    import Features from "./components/Features.svelte";

    import { gsap } from "gsap";

    import { ScrollTrigger } from "gsap/ScrollTrigger";
    import { ScrollToPlugin } from "gsap/ScrollToPlugin";

    gsap.registerPlugin(ScrollTrigger, ScrollToPlugin);
</script>

<main class="selection:bg-primary selection:text-base-100">
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
    <div id="section1" class="h-screen flex gap-5">
        <About />
    </div>
    <div id="section2" class="h-screen flex bg-base-300 overflow-x-hidden">
        <Pricing />
        <Features />
    </div>
</main>

<style>
</style>
