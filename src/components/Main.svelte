<script>
    import Step from "./Step.svelte";
    let linkedin = "https://www.linkedin.com/in/sai-roopesh/";

    let steps = [
        {
            name: "Kidney Disease Classification",
            icon: "fa fa-laptop-code",
            href: "https://github.com/Sai-Roopesh/kidney-disease-classification",
        },
        {
            name: "Pdf 2 Audio",
            icon: "fa-solid fa-file-pdf",
            href: "https://github.com/Sai-Roopesh/pdf2audio",
        },
        {
            name: "Staying-Alive",
            icon: "fa-solid fa-house-fire",
            href: "https://github.com/Sai-Roopesh/staying-alive",
        },
    ];

    let benefits = [
        {
            name: "ML Enthusiast",
            description:
                "Passionate about machine learning, constantly exploring and implementing new algorithms and models to solve real-world problems. Always eager to learn and apply the latest advancements in the field.",
        },
        {
            name: "Full Stack Developer",
            description:
                "Experienced in both front-end and back-end development, proficient in various frameworks and technologies. Skilled in building robust, scalable, and user-friendly applications from concept to deployment.",
        },
        {
            name: "Excellent Communicator",
            description:
                "Strong verbal and written communication skills, able to convey complex technical concepts to non-technical stakeholders. Effective in team collaboration, client interactions, and documentation.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center gap-10 text-center lg:text-left md:gap-8"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi I'm <span class="poppins text-violet-400">Sai</span> Roopesh.
                <br />
                <span class="poppins text-violet-400">Full Stack Developer</span
                >
                and
                <span class="poppins text-violet-400">ML Enthusiast</span>.
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="poppins text-violet-400">favorite tech</span>
                includes
                <span class="poppins text-orange-400">svelte and svelteKit</span
                >,
                <span class="poppins text-blue-400">React</span>,
                <span class="poppins text-green-400">Node.js</span>,
                <span
                    class="bg-gradient-to-r from-yellow-400 to-blue-400 text-gradient"
                    >Python!</span
                >
            </p>
        </div>

        <div class="relative shadow-2xl grid place-items-center opacity-70">
            <div class="relative">
                <img
                    src="/images/roopesh.png"
                    alt="Profile Image of Sai Roopesh"
                    class="object-cover z-[1] max-h-[70vh]"
                />
                <div
                    class="absolute inset-0 z-[2] pointer-events-none fade-overlay"
                ></div>
            </div>
        </div>
    </section>
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">My Projects.</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                <span class="poppins text-violet-400">Check </span>them out!
            </h3>
        </div>
        <a
            href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
        >
            <i class="fa-regular fa-circle-play"></i>
            <p>Watch the video!</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    This project is a classification model that predicts type of
                    kidney disease using <strong class="text-violet-400"
                        >tensorflow</strong
                    >.
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    pdf 2 audio converts pdf files to audio files using <strong
                        class="text-violet-400"
                        >Google Text to Speech API</strong
                    > available in the google cloud platform.
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    Staying-Alive is a project that uses <strong
                        class="text-violet-400">sqLite</strong
                    >
                    and <strong class="text-violet-400">Flask</strong> to create
                    a server that helps people during disasters by capturing their
                    Geolocation.
                </p>
            </Step>
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-8"
        >
            <h6 class="text-xl sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            Iam . . .
        </p>
        <div class="flex flex-col gap-20 mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-7">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        {index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3
                            class="text-2xl sm:text-3xl md:text-5xl text-violet-400"
                        >
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>

<style>
    .fade-overlay {
        background: radial-gradient(
            circle,
            rgba(0, 0, 0, 0) 60%,
            rgba(0, 0, 0, 0.7) 100%
        );
    }
</style>
