<script>
  let bg = 'bg-amber-100';
</script>

<div class="h-full w-full {bg}">
  <div class="w-full md:w-3/4 lg:w-1/2 xl:w-1/3 mx-auto">
    <div class="px-4 pt-3 text-lg font-semibold tracking-wide">
      The Lone Minstrel
    </div>
    <div class="px-4 pt-3">
      <span class="my-2 z-0 inline-flex shadow-sm rounded-md">
        <button
          type="button"
          on:click={() => (bg = 'bg-amber-100')}
          class="relative inline-flex items-center px-4 py-1 rounded-l-md border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:z-10 focus:outline-none focus:ring-1 focus:ring-gray-500 focus:border-gray-500"
        >
          Classic
        </button>
        <!--
    <button
      type="button"
      on:click={() => (bg = 'bg-black')}
      class="-ml-px relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:z-10 focus:outline-none focus:ring-1 focus:ring-indigo-500 focus:border-indigo-500"
    >
      Contemporary
    </button>
    -->
        <button
          type="button"
          on:click={() => (bg = 'bg-gray-100')}
          class="-ml-px relative inline-flex items-center px-4 py-1 rounded-r-md border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:z-10 focus:outline-none focus:ring-1 focus:ring-gray-500 focus:border-gray-500"
        >
          Modern
        </button>
      </span>
    </div>
    <div class="my-3 flex flex-col md:flex-row">
      <div class="px-4">
        <img
          class="w-full"
          alt="a painting with frame"
          src={bg === 'bg-amber-100'
            ? './lone-classic.png'
            : bg === 'bg-gray-100'
            ? './lone-min.png'
            : bg === 'bg-black'
            ? './lone-con.png'
            : ''}
        />
        <!-- <div class="my-5 relative text-left">
          <img
            class="h-28 md:h-40 drop-shadow-md"
            alt="A plaque with a painting"
            src="./plaque.png"
          />
          <div class="absolute top-3 left-3">
            <h1
              class="text-[0.9rem] md:text-[1.2rem] tracking-wide font-semibold"
            >
              The Lone Minstrel
            </h1>
            <h2 class="text-[0.8rem] md:text-[1rem] italic">oil on canvas</h2>
          </div>
          <div class="text-[0.55rem] md:text-[0.7rem] absolute bottom-3 left-3">
            On loan from <span class="italic font-semibold"
              >The Royal Trust</span
            >
          </div>
        </div> -->
      </div>
      <!-- <div class="text-black font-bold w-full md:w-3/4 px-4 md:px-0">
      Other Works of Art
      <div class="grid grid-cols-2">
        <div class="w-40 h-40 bg-white border border-black rounded-md">1</div>
        <div class="w-1/2">2</div>
        <div class="w-1/2">3</div>
        <div class="w-1/2">3</div>
      </div>
    </div> -->
    </div>
    <h1 class="px-4 pt-3 font-semibold" >
      Other Works of Art (Excuse our dust, work in progress)
    </h1>
    <div class="px-4 pt-3 grid grid-cols-2 gap-3">
      <div class={"rounded-sm flex flex-row h-12 w-auto items-center justify-center " + (bg === 'bg-amber-100' ? "border-4 border-amber-700" : "border-4 border-black")}>
          <a class="cursor-pointer" href="https://thestreamingguide.com" target="_blank">
          TSG</a>
      </div>
      <div class={"rounded-sm flex flex-row h-12 w-auto items-center justify-center " + (bg === 'bg-amber-100' ? "border-4 border-amber-700" : "border-4 border-black")}>
        <a class="cursor-pointer" href="https://mushroom.party" target="_blank">
          Mushroom Party</a>
      </div>
      <div class={"rounded-sm flex flex-row h-12 w-auto items-center justify-center " + (bg === 'bg-amber-100' ? "border-4 border-amber-700" : "border-4 border-black")}>
        Founder Anonymous
      </div>
      <div class={"rounded-sm flex flex-row h-12 w-auto items-center justify-center " + (bg === 'bg-amber-100' ? "border-4 border-amber-700" : "border-4 border-black")}>
        Scacchi
      </div>
    </div>
    <div class="h-80" />
  </div>
</div>
