<script>
    import { onMount } from 'svelte';
    export let graph;
    export let year;
    onMount(() => {
        let days = [];
        graph.weeks.map(week => 
            week.contributionDays.map(day => day.date.startsWith("2022") ? days.push(day) : null)
        )
        const squares = document.querySelector('.squares');
        for (const day of days) {
            squares.insertAdjacentHTML('beforeend', `<li data-level="${day.contributionLevel}" class="hover:bg-[] hover:cursor-pointer rounded-[2px] sm:rounded group relative flex flex-col items-center">
            <div class="absolute bottom-0 flex-col items-center hidden mb-6 sm:group-hover:flex !opacity-100">
            <span class="relative rounded-[4px] z-50 py-1 px-[5px] text-xs w-36 text-center leading-none text-white whitespace-no-wrap bg-[#25292E]">
                ${day.date}
            </span>
            <div class="w-3 h-3 -mt-2 rotate-45 bg-[#25292E]">
            </div>
            </div>
            </li>`);
        }
    });
</script>

<div class="flex flex-row text-white border border-gray-800 rounded-xl w-fit p-5 mt-5">
    <div class="flex flex-col">
        <div class="flex flex-row justify-between mb-4">
            <div class="flex flex-col">
                <div class="text-2xl font-semibold">
                    Proof of Work
                </div>
                <div class="text-gray-400">
                    My Github contributions
                </div>
            </div>
            <div class="flex flex-col text-right">
                <div class="text-gray-400">
                    Total Contributions
                </div>
                <div class="text-xl font-semibold">
                 {graph.totalContributions}
                </div>
            </div>
        </div>
        <div class="flex flex-row-reverse">
        <div class="flex flex-col ml-5 gap-2">
            <div class={`rounded-full ${year === '2022' ? "bg-[#161b22]" : "bg-black"}  px-8 py-1 text-sm cursor-pointer`}>2022</div>
            <div class={`rounded-full ${year === '2021' ? "bg-[#161b22]" : "bg-black"}  px-8 py-1 text-sm`}>2021</div>
        </div>
        <div>
        <div class="">
            <ul class="months w-fit mb-2 text-sm">
                <li>Jan</li>
                <li>Feb</li>
                <li>Mar</li>
                <li>Apr</li>
                <li>May</li>
                <li>Jun</li>
                <li>Jul</li>
                <li>Aug</li>
                <li>Sep</li>
                <li>Oct</li>
                <li>Nov</li>
                <li>Dec</li>
            </ul>
            <ul class="squares">
            </ul>
        </div>
        <div class="flex flex-row mt-5 justify-start items-center">
            <h4 class="mr-3">
                Less
            </h4>
            <div class="w-[14px] h-[14px] rounded-[2px] mr-[2px] bg-[#161b22]">
            </div>
            <div class="w-[14px] h-[14px] rounded-[2px] mr-[2px] bg-[#a3d4ff]">
            </div>
            <div class="w-[14px] h-[14px] rounded-[2px] mr-[2px] bg-[#46a9ff]">
            </div>
            <div class="w-[14px] h-[14px] rounded-[2px] mr-[2px] bg-[#007ce9]">
            </div>
            <div class="w-[14px] h-[14px] rounded-[2px] mr-[2px] bg-[#004B8D]">
            </div>
            <h4 class="ml-3">
                More
            </h4>
        </div>
        </div>
        </div>
    </div>
</div>