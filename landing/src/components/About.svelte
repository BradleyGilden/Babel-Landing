<script>
    import gsap from "gsap";
    import ChatBubble from "./ChatBubble.svelte";
    import { onMount } from "svelte";

    onMount(() => {
        gsap.from('.chat', {
            y: '-200vh',
            stagger: 1,
            duration: 8,
            ease: 'power2',
            scrollTrigger: {
                trigger: '#section1',
                scrub: 1,
                toggleActions: 'play pause resume reset',
                pin: true,
            }
        })
    })
</script>

<div id="about" class="w-1/2 items-center flex flex-col">
    <h1 class="text-[2.5rem] font-mserrat w-full text-center mb-2 hover:skew-x-6 transition-all mt-[25vh]">
        About
    </h1>
    <p class="w-3/4 text-xl hover:skew-x-6 transition-all">
        Babel Chat is a revolutionary live chat application that breaks
        down language barriers in real-time. With its cutting-edge
        translation technology, users can communicate seamlessly with
        people from different linguistic backgrounds. Say goodbye to
        misunderstandings and embrace a world where language is no
        longer a hindrance to connection.
    </p>
</div>
<div id="chat-show" class="w-1/2 flex flex-col justify-center px-5">
    <ChatBubble start={true} placeholder={'K'} name={'Katnis Everdeen'}  time={'12:45'}
        message={'May the odds be forever in your favour!'}
    />
    <ChatBubble start={false} placeholder={'E'} name={'Ezio Auditor'}  time={'12:50'}
        message={'لا شيء واقع مطلق بل كل ممكن'}
    />
    <ChatBubble start={true} placeholder={'M'} name={'Marie Curie'}  time={'13:15'}
        message={"Dans la vie, il n'y a rien à craindre, il n'y a qu'à comprendre. C'est maintenant le moment de comprendre davantage, pour pouvoir moins craindre."}
    />
    <ChatBubble start={false} placeholder={'S'} name={'Srinivasa Ramanujan'}  time={'18:22'}
        message={'எனக்கான சமன்பாடு கடவுளைப் பற்றிய எண்ணத்தை வெளிப்படுத்தாத வரையில் எந்த அர்த்தமும் இல்லை'}
    />
</div>