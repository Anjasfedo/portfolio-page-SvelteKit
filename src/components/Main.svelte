<script>
    import Step from "../components/Step.svelte";

    let steps = [
        { name: "Lorem", icon: "fa-solid fa-cart-shopping" },
        { name: "Ipsum", icon: "fa-solid fa-list-check" },
        { name: "Dolor", icon: "fa-solid fa-diagram-project" },
    ];

    let benefits = [
        {
            name: "Lorem",
            description:
                "Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, est. Accusamus ullam dicta nam molestiae nesciunt hic, culpa animi, tempore corrupti obcaecati incidunt molestias sequi quia voluptatum ad cum nulla?",
        },
        {
            name: "Ipsum",
            description:
                "Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, est. Accusamus ullam dicta nam molestiae nesciunt hic, culpa animi, tempore corrupti obcaecati incidunt molestias sequi quia voluptatum ad cum nulla?",
        },
        {
            name: "Dolor",
            description:
                "Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, est. Accusamus ullam dicta nam molestiae nesciunt hic, culpa animi, tempore corrupti obcaecati incidunt molestias sequi quia voluptatum ad cum nulla?",
        },
    ];
</script>

lorem
<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Anjas</span>Fedo <br />Full Stack
                <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">Favorite Tech</span> includes JavaScript (Next.JS or SvelteKit), TailwindCSS,
                Node.JS + Express.JS & MongoDB or Firebase/Firestore
            </p>
            <a
                href="#"
                target="_blank"
                class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                ></div>
                <h4 class="relative z-10">Get in touch &rarr;</h4></a
            >
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/img-blank.PNG"} alt="Profile Image" class="object-cover z-[2] max-h-[70vh]" />
        </div>
    </section>
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">A few of my creative</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">See</span> My Work?
            </h3>
        </div>
        <a
            href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
            ><i class="fa-regular fa-circle-play"></i>
            <p>Watch The Video</p></a
        >
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sit temporibus, <strong
                        class="text-violet-400"
                        >repudiandae fugit similique voluptatibus enim rem sed consequatur iste fuga culpa dolor?</strong
                    > Harum ipsum inventore vel voluptates fugiat repellendus aliquam?
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sit temporibus, <strong
                        class="text-violet-400"
                        >repudiandae fugit similique voluptatibus enim rem sed consequatur iste fuga culpa dolor?</strong
                    > Harum ipsum inventore vel voluptates fugiat repellendus aliquam?
                </p></Step
            ><Step step={steps[2]}>
                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sit temporibus, <strong
                        class="text-violet-400"
                        >repudiandae fugit similique voluptatibus enim rem sed consequatur iste fuga culpa dolor?</strong
                    > Harum ipsum inventore vel voluptates fugiat repellendus aliquam?
                </p></Step
            >
        </div>
    </section>
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to Know More?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">About</span> Me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-50 font-semibold">0{index + 1}</p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">{benefit.name}</h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">
            The <span class="text-violet-400 poppins">Complete</span> Package
        </h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class="border-b border-solid border-slate-200">
                    <tr>
                        <th></th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">Me</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200e">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
                            >Dedication</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200e">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
                            >Critical Thought</td
                        >
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200e">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
                            >Interpersonal Skills</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200e">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
                            >Programming Abiliy</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to See More &rarr;</p>
        </div>
        <p class="mx-auto">So Why Not Invest?</p>
    </section>
</main>
