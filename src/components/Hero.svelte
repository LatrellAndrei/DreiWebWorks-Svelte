<script>
    import CtAs from "./CTAs.svelte";
    import Header from "./Header.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Stars from "./Stars.svelte";
</script>

<SectionWrapper>
    <Header/>
    <div class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14">
        <h2 class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full 
         text-center font-semibold">
            <span class="text-indigo-400">Create</span>
            Websites <span class="text-slate-700 ">for Everyone!</span><br/>
            Design <span class="text-indigo-400">For All</span>

        </h2>
        <p class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full">
            Ensuring inclusive design principles means that websites can be accessed and enjoyed by people of all abilities, 
            <span class="italic">fostering a more welcoming and equitable online experience for everyone. </span>
        </p>
        <CtAs/>
   <Stars/>
    </div>
</SectionWrapper>