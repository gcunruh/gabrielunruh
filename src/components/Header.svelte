<script>
    export let page;
</script>

<header class="text-white w-full my-8 text-xs md:text-sm">
  <div class="flex flex-row rounded-full border border-gray-800 w-fit mx-auto p-1 bg-[#161b22] justify-between">
    <a href="/" class={`w-28 md:w-40 text-center rounded-full py-2 ${page.path === "/" ? "bg-[#007ce9]/80" : ""}`}>Home</a>
    <a href="/cv" class={`w-28 md:w-40 text-center rounded-full py-2 ${page.path === "/cv" ? "bg-amber-500/80" : ""}`}>Experience</a>
    <a href="https://cerebration.medium.com/" target="_blank" rel="noopener noreferrer" class={`w-28 md:w-40 rounded-full text-center py-2 ${page.path === "/swissarmyknife" ? "bg-rose-500/80" : ""}`}>Writing</a>
  </div>
</header>
