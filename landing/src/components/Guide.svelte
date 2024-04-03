<script>
    import gsap from "gsap";
</script>


<a 
    class="fixed btn btn-sm btn-primary rounded-full z-50 right-20 bottom-10 font-bold"
    href="https://chat.bradleygilden.tech"
    target="_blank"
    rel="noopener noreferrer"
>
    Get Started
</a>
<button 
    class="fixed bg-base-300 text-primary rounded-full h-8 w-8 z-50 right-10 bottom-10"
    on:click={() => {gsap.to(window, {duration: 0.8, scrollTo: '#navbar' })}}
>
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"><path d="M12 8.36853L20.9679 13.1162L20.0321 14.8838L12 10.6315L3.96788 14.8838L3.0321 13.1162L12 8.36853Z"></path></svg>
</button>