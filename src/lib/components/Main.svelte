<!-- Main.svelte -->
<script>
    // export let propName; // Example: export any props you need
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Fella</span> <br/>the <span class="poppins text-violet-400">Canada Goose</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favourite food</span> includes grasses and wheatseed!
            </p>
            <a 
                class="blueShadow mx-auto lg:mr-auto text-base sm:txt-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" 
                href="https://www.rspb.org.uk/birds-and-wildlife/canada-goose" 
                target="_blank"
            >
                <div 
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Goose facts &rarr;</h4>
            </a>
        </div>
    </section>
</main>