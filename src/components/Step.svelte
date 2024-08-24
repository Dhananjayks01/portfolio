<script>
    export let step;
</script>

<a href={step.href} target="_blank" class="max-w-md p-6 border border-violet-700 hover:border-violet-400 duration-200 rounded-lg shadow bg-transparent cursor-pointer flex flex-col gap-2">
    <img src={`images/${step.icon}`} alt={step.name} class="w-7 h-7" />
    <h5 class="text-2xl font-semibold tracking-tight text-gray-900 dark:text-white">
        {step.name}
    </h5>
    <slot />
    <div class="inline-flex font-medium items-center text-violet-700 hover:underline">
        Demo Link
        <svg class="w-3 h-3 ms-2.5 rtl:rotate-[270deg]" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 18 18">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11v4.833A1.166 1.166 0 0 1 13.833 17H2.167A1.167 1.167 0 0 1 1 15.833V4.167A1.166 1.166 0 0 1 2.167 3h4.618m4.447-2H17v5.768M9.111 8.889l7.778-7.778"/>
        </svg>
    </div>
</a>