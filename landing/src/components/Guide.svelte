<script>
    import gsap from "gsap";
</script>

<button 
    class="fixed btn btn-primary rounded-full h-16 w-16 z-50 right-10 bottom-10"
    on:click={() => {gsap.to(window, {duration: 0.8, scrollTo: '#navbar' })}}
>
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"><path d="M12 8.36853L20.9679 13.1162L20.0321 14.8838L12 10.6315L3.96788 14.8838L3.0321 13.1162L12 8.36853Z"></path></svg>
</button>