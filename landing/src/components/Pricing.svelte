<script>
    import gsap from "gsap";
    import { onMount } from "svelte";

    onMount(() => {
        let tl = gsap.timeline({ repeat: -1, ease: "power1", yoyo: true });

        tl.to("#banner-text", {
            color: "blue",
            duration: 0.3,
        })
            .to("#banner-text", {
                color: "red",
                duration: 0.3,
            })
            .to("#banner-text", {
                color: "green",
                duration: 0.3,
            });
    });
</script>

<div id="pricing" class="h-full bg-warning w-[100vw] text-warning-content">
    <h1 class="text-[2.5rem] text-center mt-10 font-mserrat mb-10">Pricing</h1>

    <h2 id="banner-text" class="text-[3rem] font-mserrat text-center">
        This software is currently FREE TO USE!
    </h2>

    <div
        class="text-warning bg-warning-content rounded-2xl p-3 w-1/2 text-xl mx-auto mt-20"
    >
        <h2 class="text-2xl underline-offset-4 w-full text-center">
            The Mission
        </h2>
        <p>
            It is my goal to make as much 0 - low cost applications as I can for
            everyone to use. Please support my efforts by buying me a cup of joe
            :)
        </p>
    </div>

    <img id="qr-code" class="w-[10rem] h-[10rem] mx-auto mt-10" src="/coffee.png" alt="buy me a coffee" />
</div>
