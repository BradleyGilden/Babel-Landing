<script>
    import gsap from "gsap";
    import { onMount } from "svelte";

    onMount(() => {
        gsap.to("#features", {
            x: "-200vw",
            duration: 3,
            ease: "power2",
            delay: 0.5,
            scrollTrigger: {
                trigger: "#section2",
                start: "+=5",
                scrub: 1,
                toggleActions: "play pause resume reset",
                pin: true,
                snap: {
                    snapTo: [0, 0.1, 0.2, 0.3, 0.4, 0.8, 1],
                    duration: 0.8,
                    delay: 0.1,
                    ease: "power1.inOut",
                },
            },
        });
    });
</script>

<div id="features" class="h-full bg-info w-[100vw] ml-[-100vw] text-base-100">
    <h1 class="text-[2.5rem] text-center mt-10 font-mserrat mb-10">Features</h1>
    <div class="text-primary flex flex-wrap justify-center items-center gap-10 w-1/2 mx-auto">
        <div class="bg-base-300 rounded-2xl p-5 w-[20rem]">
            <h2 class="text-2xl mb-2">Private Messaging</h2>
            <p>
                Babel Chat supports private messaging to communicate privately
                between users. Private Rooms support
            </p>
        </div>
        <div class="bg-base-300 rounded-2xl p-5 w-[20rem]">
            <h2 class="text-2xl mb-2">Global Chat Rooms</h2>
            <p>
                Freely connect with others in a global chat room. Global chat rooms
                have no user limit or restrictions.
            </p>
        </div>
        <div>
            <h2 class="text-2xl mb-2 text-base-300 text-center font-semibold">Live Translation</h2>
            <p class="mb-2 text-base-300 text-center font-semibol"> The main feature of the chat app is it's ability to translate in real time. Helping break communication
                barriers between people
            </p>
            <div class="diff h-[8rem] w-[40rem] rounded-2xl">
                <div class="diff-item-1 text-base-300 font-semibold">
                    <div class="chat chat-start">
                        <div class="avatar placeholder">
                            <div class="bg-neutral text-neutral-content rounded-full w-10">
                              <span class="text-md">K</span>
                            </div>
                        </div>
                        <div class="chat-header">
                          Kim
                          <time class="text-xs opacity-50">12:45</time>
                        </div>
                        <div class="chat-bubble">
                            Did you know the population of the earth is estimated to be over
                            8 billion people? That's a lot of potential chat buddies!
                        </div>
                    </div>
                </div>
                <div class="diff-item-2 bg-base-300 text-neutral-content">
                    <div class="chat chat-start">
                        <div class="avatar placeholder">
                            <div class="bg-neutral text-neutral-content rounded-full w-10">
                              <span class="text-md">K</span>
                            </div>
                        </div>
                        <div class="chat-header">
                          Kim
                          <time class="text-xs opacity-50">12:45</time>
                        </div>
                        <div class="chat-bubble">
                            Tahukah kamu perkiraan populasi bumi lebih dari 8 miliar orang?
                            Itu banyak sekali teman mengobrol potensial!
                        </div>
                    </div>
                </div>
                <div class="diff-resizer"></div>
            </div>
        </div>
    </div>
</div>
