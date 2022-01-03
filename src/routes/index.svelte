<script>
  let bg = 'bg-yellow-100';
</script>

<div class="h-screen {bg}">
  <div class="container mx-auto px-4 ">
    <div class="flex justify-end">
      <span class="my-2 z-0 inline-flex shadow-sm rounded-md">
        <button
          type="button"
          on:click={() => (bg = 'bg-yellow-100')}
          class="relative inline-flex items-center px-4 py-2 rounded-l-md border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:z-10 focus:outline-none focus:ring-1 focus:ring-indigo-500 focus:border-indigo-500"
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
          on:click={() => (bg = 'bg-white')}
          class="-ml-px relative inline-flex items-center px-4 py-2 rounded-r-md border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:z-10 focus:outline-none focus:ring-1 focus:ring-indigo-500 focus:border-indigo-500"
        >
          Modern
        </button>
      </span>
    </div>
    <img
      class="w-full my-5 mx-auto max-w-screen-md"
      alt="a painting with frame"
      src={bg === 'bg-yellow-100'
        ? './lone-classic.png'
        : bg === 'bg-white'
        ? './lone-min.png'
        : bg === 'bg-black'
        ? './lone-con.png'
        : ''}
    />
    <div class="bg-white w-40 shadow-sm">
      <h1>The Lone Minstral</h1>
      <h2>oil on canvas</h2>
    </div>
  </div>
</div>
