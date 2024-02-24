<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    let faqs = [
    {
        question: "Do you offer hosting services for websites?",
        ans: "Drei Web Works primarily focuses on website design and development. While we don't provide hosting services directly, we can recommend reliable hosting providers and assist with the setup and configuration process."
    },
    {
        question: "Can you create multilingual websites?",
        ans: "Yes, we have experience creating multilingual websites to cater to diverse audiences. We can implement language switchers and localization features to ensure that your website is accessible and user-friendly for visitors from different regions."
    },
    {
        question: "What payment methods do you accept for your services?",
        ans: "We accept various payment methods, including credit/debit cards, bank transfers, and PayPal. Our billing process is transparent, and we provide detailed invoices for all services rendered."
    },
    {
        question: "Do you provide training on how to manage and update the website?",
        ans: "Yes, we offer training sessions to empower clients to manage and update their websites independently. We provide tutorials and documentation tailored to your specific content management system (CMS) or website platform."
    },
    {
        question: "What happens if I encounter issues with my website after it's launched?",
        ans: "We provide post-launch support to address any technical issues or concerns that may arise after your website goes live. Our support team is available to assist you promptly and ensure that your website operates smoothly."
    },
    {
        question: "Can you integrate third-party tools and services into my website?",
        ans: "Yes, we can integrate various third-party tools and services into your website, including payment gateways, customer relationship management (CRM) systems, email marketing platforms, and analytics tools. We ensure seamless integration and compatibility with your existing infrastructure."
    },
    {
        question: "Is there a minimum project size or budget requirement?",
        ans: "We work with clients of all sizes and budgets, from small businesses to large corporations. There is no minimum project size or budget requirement. We tailor our solutions to meet your specific needs and objectives, regardless of the scale of the project."
    },
    {
        question: "Can you provide examples of your previous work/portfolio?",
        ans: "Yes, we can provide examples of our previous work and portfolio upon request. We have successfully completed projects for clients across various industries, showcasing our expertise in website design and development."
    },
    {
        question: "Do you offer ongoing support and maintenance plans?",
        ans: "Yes, we offer ongoing support and maintenance plans to ensure that your website remains secure, up-to-date, and optimized for performance. Our plans include regular software updates, security audits, and proactive monitoring to prevent potential issues."
    },
    {
        question: "What is your process for handling website security and data privacy?",
        ans: "We take website security and data privacy seriously. We implement industry best practices, such as encryption protocols, secure login mechanisms, and regular security audits, to safeguard your website and sensitive information from unauthorized access and breaches."
    }
];

</script>

<SectionWrapper id="faqs">
    <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center">
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">Where Answers Await</p>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"> 
                Frequently Asked Questions
            </h3>
            
        </div>
        <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
            {#each faqs as faq }
                <div class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6">
                        <div class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"></div>
                        <div class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"></div>
                        <h4 class="text-lg sm:text-xl md:text-2xl pt-2">{faq.question}</h4>
                        <p class="pl-2">{faq.ans}</p>
                </div>
            {/each}
        </div>
        </div>
</SectionWrapper>