<script>
    import ProductCard from "./ProductCard.svelte"
    import SectionWrapper  from "./SectionWrapper.svelte";
    let productFeatures = [
    {
        featureList: [
            "Customized design based on your preferences",
            "Responsive and mobile-friendly layouts",
            "Integration of multimedia content (images, videos, etc.)",
            "Search engine optimization (SEO) to improve visibility",
        ],
        description: "Our websites are tailored to your brand identity and optimized for user engagement and conversion.",
        imgUrl: "assets/design.png",
        
    },
    {
        featureList: [
            "Development using popular JavaScript frameworks ",
            "Modular and scalable architecture for easy expansion",
            "Efficient codebase for faster loading times",
            "Integration of advanced features and functionalities",
        ],
        description: "Utilize the power of modern JavaScript frameworks for dynamic and interactive user experiences.",
        imgUrl: "assets/frameworks.png",
    },
    {
        featureList: [
            "Custom development for unique functionalities",
            "E-commerce integration for online stores",
            "Social media integration to expand your reach",
            "Analytics to track website performance",
        ],
        description: "We offer custom development options to meet your specific requirements and help you achieve your online goals.",
        imgUrl: "assets/development.png",
    }
];

    
</script>
<!---Product-->
<SectionWrapper id="project">
<div class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14">
    <div class="flex flex-col gap-2">
        <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
            Start now <span class="text-indigo-400">Design with Us</span> Today!
        </p>
        <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">
            Features for Everyone!</h3>
    </div>
    <!--this code is for showing the title of description-->
        {#each productFeatures as productFeature, index}
            <ProductCard {productFeature} {index}>
                {#if index === 0}
                Experience the best website  <span class= "text-indigo-400 font-medium">design </span> for everyone 
                {:else if  index  === 1}
                 <span class="text-indigo-400 font-medium">Drei Web Works</span><br/> will Help you
                {:else}
                Give us your best ideas <span class="text-indigo-400 font-medium">Web Design</span>
                and <span class="text-indigo-400 font-medium">Development</span>
                {/if}
            </ProductCard>
        {/each}
    </div>
</SectionWrapper>