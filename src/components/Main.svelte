<script>
    import Step from "./Step.svelte"
    let steps = [
        {name:'Inspire Bubble', icon:'fa-solid fa-icons', href:'https://inspire-bubble.vercel.app/'}, //add icon of your choice
        {name:'Urban Listing', icon:'fa-solid fa-house', href:'https://urbanlisting.vercel.app/'},
        {name:'College Shortlist Advice', icon:'fa-solid fa-graduation-cap', href:'https://nidhiyashwanth.github.io/College-Shortlist-Advice/'}
    ];
    let benefits = [
        {name: 'a self-taught developer, fueled with passion', description: 'As a self-taught developer, I am fueled with passion for crafting innovative solutions and pushing the boundaries of what technology can achieve. My journey into the world of coding has been driven by an intrinsic love for problem-solving and a relentless pursuit of knowledge. This passion not only motivates me to continuously expand my skill set but also empowers me to approach each project with enthusiasm and creativity. From learning to code independently to applying my skills in real-world scenarios, my commitment to self-directed growth is rooted in a genuine and unwavering love for the art and science of software development.'},
        {name: 'a product design & UX fanatic', description: 'I am deeply passionate about product design and user experience (UX). Beyond writing code, I thrive on crafting digital experiences that are not just functional but also intuitive and aesthetically pleasing. With a keen eye for design principles and user-centric thinking, I ensure that the products I work on deliver a seamless and delightful user experience.'},
        {name: 'an excellent communicator', description: 'Effective communication is at the core of successful collaboration and project development. I pride myself on being an excellent communicator, whether it\'s conveying complex technical concepts to non-technical stakeholders or collaborating with cross-functional teams. My ability to articulate ideas and actively listen ensures a smooth and productive workflow in any project environment.'}
    ]
</script>
<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-0 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-0 lg:gap-10 ">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! This is Nidhi<span class="poppins text-violet-400">Yashwanth</span><br/> Full Stack <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favourite tech</span> includes <span class="text-violet-400">Python, JavaScript, TypeScript, Next.js, React.js, MongoDB, Node.js, Express.js</span> and many more frameworks and tools I pickup while working.
            </p>
            <a class="blueShadow mx-auto lg:mr-auto lg:ml-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" href="https://www.linkedin.com/in/nidhiyashwanth/" target="_blank">
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative grid place-items-center">
            <img src={"images/Picsart_23-11-10_15-09-34-207.png"} alt="Profile logo" class="object-cover z-[2] max-h-[70vh]"/>
        </div>
    </section>
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endeavours
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
            
        </div>
        <!-- <a href="#" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:bg-violet-700 duration-200">
            <i class="fa-regular fa-circle-play"></i>
            <p>
                Watch the video
            </p>
        </a> -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Inspire Bubble is a hriving developer community for showcasing creativity and innovation. Built using <strong class="text-violet-400">Next.js, Tailwind CSS, Firebase, GraphQL, Grafbase!</strong> Next.js is a javascript framework, Tailwind is used for styling.</p>
            </Step>
            <Step step={steps[1]}>
                <p>Urban Listing is a hriving developer community for showcasing creativity and innovation. Built using <strong class="text-violet-400">Next.js, Tailwind CSS, Firebase, GraphQL, Grafbase!</strong> Next.js is a javascript framework, Tailwind is used for styling.</p>
            </Step>
            <Step step={steps[2]}>
                <p>College Shortlist Advice is a hriving developer community for showcasing creativity and innovation. Built using <strong class="text-violet-400">Next.js, Tailwind CSS, Firebase, GraphQL, Grafbase!</strong> Next.js is a javascript framework, Tailwind is used for styling.</p>
            </Step>
        </div>
    </section>
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl ">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am ...</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
            <div class="flex gap-6 sm:gap-8">
                <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                    0{index + 1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-xl sm:text-2xl md:text-4xl">
                        {benefit.name}
                    </h3>
                    <p class="">{benefit.description}</p>
                </div>
            </div>
            {/each}
        </div>
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-violet-400 poppins">Complete</span> Package</h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class="border-b border-solid border-slate-200">
                    <tr class="">
                        <th/>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">Me</th>
                    </tr>
                </thead>
                <tbody class="border-b border-solid border-slate-200">
                    <tr>
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">
                        Dedication
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-xmark text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-green-500"></i>
                    </td>
                </tr>
                    <tr>
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">
                        Critical Thinking
                    </td>
                    <td>
                        <i class="fa-solid fa-xmark text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-green-500"></i>
                    </td>
                </tr>
                    <tr>
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">
                        Interpersonal Skills
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-xmark text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-green-500"></i>
                    </td>
                </tr>
                    <tr>
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">
                        Programming Ability
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-xmark text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-slate-500"></i>
                    </td>
                    <td>
                        <i class="fa-solid fa-check text-green-500"></i>
                    </td>
                </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto">So why not connect?</p>
    </section>
    <section id="" class="mb-44 flex flex-col items-center justify-center">
        <p id="blog" class="pt-20 text-5xl poppins text-center">Coming soon <span class="text-violet-400 font-bold">I promise </span>😊</p>
        <img src={"images/under.svg"} alt="gif" class="w-1/2 mt-24 -py-24 object-cover z-[2] max-h-[70vh] sm:h-3/4 md:h-3/5"/>
    </section>
</main>