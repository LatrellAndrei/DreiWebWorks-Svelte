<script>
    import ReviewCard from "./ReviewCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte"
    import Stars from "./Stars.svelte";
    let lim = true;
    let reviewsList = [
    {
        name: "John Doe",
        review: "Drei Web Works has been instrumental in establishing my online presence! The website they designed for me is not only visually stunning but also highly functional. Their attention to detail and responsiveness to my needs have made the entire process seamless.",
        features: [
            "Visually stunning design",
            "Highly functional website",
            "Attention to detail",
            "Responsive customer service",
        ],
    },
    {
        name: "Jane Smith",
        review: "I couldn't be happier with the website Drei Web Works created for my business. It perfectly captures the essence of what I do and has significantly boosted my online visibility. The team's expertise and dedication are evident in every aspect of the site.",
        features: [
            "Captures essence of business",
            "Boosted online visibility",
            "Expertise",
            "Dedication",
        ],
    },
    {
        name: "Michael Brown",
        review: "Choosing Drei Web Works to develop my website was one of the best decisions I've made for my business. The site they built is not only aesthetically pleasing but also easy to navigate, which has resulted in increased user engagement and conversions.",
        features: [
            "Aesthetically pleasing design",
            "Easy navigation",
            "Increased user engagement",
            "Improved conversions",
        ],
    },
    {
        name: "Sarah Williams",
        review: "Drei Web Works exceeded my expectations with the website they created for me. It's user-friendly, visually appealing, and has helped me attract more clients to my business. I appreciate their creativity and commitment to delivering top-notch results.",
        features: [
            "User-friendly design",
            "Visually appealing",
            "Attracts more clients",
            "Creativity",
            "Commitment to quality",
        ],
    },
    {
        name: "David Lee",
        review: "I'm thoroughly impressed with the level of professionalism displayed by Drei Web Works throughout the website development process. They took the time to understand my goals and delivered a website that not only meets but exceeds my expectations.",
        features: [
            "Professionalism",
            "Understanding of client goals",
            "Exceeds expectations",
            "Attention to client needs",
        ],
    },
    {
        name: "Ashley Johnson",
        review: "Working with Drei Web Works has been a pleasure from start to finish. They were responsive to my ideas and provided valuable insights to enhance the functionality of my website. I highly recommend their services to anyone in need of a reliable web design partner.",
        features: [
            "Responsive to client ideas",
            "Valuable insights",
            "Enhanced website functionality",
            "Reliable service",
        ],
    },
    {
        name: "Mark Robinson",
        review: "Drei Web Works transformed my vision into reality with the website they created for my brand. It's not just a website; it's a powerful tool that has helped me connect with my audience and grow my business. Their expertise is unmatched!",
        features: [
            "Transformative",
            "Powerful business tool",
            "Audience connection",
            "Expertise",
        ],
    },
];

</script>

<SectionWrapper id="reviews">
    <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center">
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">Dont Just take our word for it</p>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"> 
                See What <span class="text-indigo-400"> Others</span> Have To Say
            </h3>
        </div>
        <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
            <div class="flex flex-col gap-8">
                {#each lim ?  reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                <ReviewCard {reviewItem} left = {true} {index}/>
                {/each}
            </div>
                <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
                <div class="flex flex-col gap-8">
                    {#each lim ?  reviewsList.slice(0,4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} {index}/>
                    {/each}
                </div>
            </div>
            <button on:click={() => (lim = !lim)} class="specialBtn">
                <p>{lim ? 'Show More' : 'Show Less'}</p>
                </button>
                <div class="flex flex-col gap-10">
                    <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
                        Trusted by many web designers.
                    </p>
                    <Stars/>
                </div>
    </div>
</SectionWrapper>