<script>
    import Step from "./Step.svelte"
    import Lottie from "../lib/Lottie.svelte"
    import animationData from '../assets/Animation1.json';
    let steps = [
        {
            name: 'Inspire Bubble',
            icon: 'inspire-bubble.svg', // Update with the correct SVG filename
            href: 'https://inspire-bubble.vercel.app/',
            description: 'Inspire Bubble is a thriving developer community for showcasing creativity and innovation. Built using Next.js, Tailwind CSS, Firebase, GraphQL, Grafbase! Next.js is a javascript framework, Tailwind is used for styling.'
        },
        {
            name: 'Urban Listing',
            icon: 'urban-listing.svg', // Update with the correct SVG filename
            href: 'https://urbanlisting.vercel.app/',
            description: 'Urban Listing is a full-stack web application built with React, Tailwind CSS, and Firebase. I designed a modern, user-friendly interface with responsive design for an engaging experience. Firebase powers user authentication and real-time database storage, and the application is deployed on Vercel.'
        },
        {
            name: 'College Shortlist Advice',
            icon: 'college.svg', // Update with the correct SVG filename
            href: 'https://nidhiyashwanth.github.io/College-Shortlist-Advice/',
            description: 'College Shortlist Advice is designed to help students find colleges that match their financial situation and academic achievements. I created a user-friendly interface with interactive cards that display relevant college information.'
        }
    ];
    let benefits = [
        {name: 'a self-taught developer, fueled with passion', description: 'As a self-taught developer, I am fueled with passion for crafting innovative solutions and pushing the boundaries of what technology can achieve. My journey into the world of coding has been driven by an intrinsic love for problem-solving and a relentless pursuit of knowledge. This passion not only motivates me to continuously expand my skill set but also empowers me to approach each project with enthusiasm and creativity. From learning to code independently to applying my skills in real-world scenarios, my commitment to self-directed growth is rooted in a genuine and unwavering love for the art and science of software development.'},
        {name: 'a product design & UX fanatic', description: 'I am deeply passionate about product design and user experience (UX). Beyond writing code, I thrive on crafting digital experiences that are not just functional but also intuitive and aesthetically pleasing. With a keen eye for design principles and user-centric thinking, I ensure that the products I work on deliver a seamless and delightful user experience.'},
        {name: 'an excellent communicator', description: 'Effective communication is at the core of successful collaboration and project development. I pride myself on being an excellent communicator, whether it\'s conveying complex technical concepts to non-technical stakeholders or collaborating with cross-functional teams. My ability to articulate ideas and actively listen ensures a smooth and productive workflow in any project environment.'}
    ]
    let blogSteps = [
        {name: 'Jenkins Pipeline', icon:'fa-solid fa-timeline', href:'/jenkins-blog'}
    ]
    let blogs = [
        {name: 'How to setup a pipeline to automate CI/CD using jenkins', description: 'Will write more on that here'}
    ]
</script>
<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-0 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-0 lg:gap-10 ">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! This is <br/><span class="poppins text-violet-400">Dhananjay K S</span><br/> Full Stack <span class="poppins text-violet-400">Developer</span>
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
            <img src={"images/profilepic.jpg"} alt="Profile logo" class="object-cover z-[2] max-h-[70vh]"/>
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
                <p>Inspire Bubble is a thriving developer community for showcasing creativity and innovation. Built using <strong class="text-violet-400">Next.js, Tailwind CSS, Firebase, GraphQL, Grafbase!</strong> Next.js is a javascript framework, Tailwind is used for styling.</p>
            </Step>
            <Step step={steps[1]}>
                <p>Urban Listing is a full-stack web application built with <strong class="text-violet-400">React, Tailwind CSS</strong>, and <strong class="text-violet-400">Firebase</strong>. It's a modern, user-friendly interface with responsive design for an engaging experience. Firebase powers auth and real-time database storage. </p>
            </Step>
            <Step step={steps[2]}>
                <p>College Shortlist Advice is designed to help students find colleges that match their financial situation and academic achievements. I created a user-friendly interface with interactive cards that display relevant college information.</p>
            </Step>
        </div>
    </section>
    <!-- Benefits section -->
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
    </section>

    <!-- Blog posts section -->
    <!-- <section id="" class="mb-44 flex flex-col items-center justify-center -mt-10">
        <div class="mx-10 w-full">
            <div class="max-w-md p-6 border border-violet-700 hover:border-violet-400 duration-200 rounded-lg shadow bg-transparent cursor-pointer">
                <svg class="w-7 h-7 text-gray-500 dark:text-gray-400 mb-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 20 20">
                <path d="M18 5h-.7c.229-.467.349-.98.351-1.5a3.5 3.5 0 0 0-3.5-3.5c-1.717 0-3.215 1.2-4.331 2.481C8.4.842 6.949 0 5.5 0A3.5 3.5 0 0 0 2 3.5c.003.52.123 1.033.351 1.5H2a2 2 0 0 0-2 2v3a1 1 0 0 0 1 1h18a1 1 0 0 0 1-1V7a2 2 0 0 0-2-2ZM8.058 5H5.5a1.5 1.5 0 0 1 0-3c.9 0 2 .754 3.092 2.122-.219.337-.392.635-.534.878Zm6.1 0h-3.742c.933-1.368 2.371-3 3.739-3a1.5 1.5 0 0 1 0 3h.003ZM11 13H9v7h2v-7Zm-4 0H2v5a2 2 0 0 0 2 2h3v-7Zm6 0v7h3a2 2 0 0 0 2-2v-5h-5Z"/>
                </svg>
            
                <a href="https://inspire-bubble.vercel.app/" target="_blank">
                    <h5 class="mb-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white">Inspire Bubble</h5>
                </a>
                
                <p class="mb-3 font-normal text-gray-500 dark:text-gray-400">Inspire Bubble is a thriving developer community for showcasing creativity and innovation. Built using <strong class="text-violet-400">Next.js, Tailwind CSS, Firebase, GraphQL, Grafbase!</strong> Next.js is a javascript framework, Tailwind is used for styling.</p>
            
                <a href="https://inspire-bubble.vercel.app/" target="_blank" class="inline-flex font-medium items-center text-violet-700 hover:underline">
                    Demo Link
                    <svg class="w-3 h-3 ms-2.5 rtl:rotate-[270deg]" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 18 18">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11v4.833A1.166 1.166 0 0 1 13.833 17H2.167A1.167 1.167 0 0 1 1 15.833V4.167A1.166 1.166 0 0 1 2.167 3h4.618m4.447-2H17v5.768M9.111 8.889l7.778-7.778"/>
                    </svg>
                </a>
            </div>
        </div> 
        
    </section> -->
    <section id="" class="mb-44 flex flex-col items-center justify-center">
        <p id="blog" class="pt-20 text-5xl poppins text-center">Blog coming soon <span class="text-violet-400 font-bold">I promise </span>😊</p>
        <!-- <img src={"images/under.svg"} alt="gif" class="w-1/2 mt-24 -py-24 object-cover z-[2] max-h-[70vh] sm:h-3/4 md:h-3/5"/> -->
        <div class="w-80 h-80 sm:w-[500px] sm:h-[500px]">
            <Lottie animationData={animationData}/>
        </div> 
        
    </section>
</main>