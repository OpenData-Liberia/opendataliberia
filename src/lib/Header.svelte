<script lang="ts">
  let isMenuOpen = false;
</script>

<header class="bg-primary text-white">
  <nav class="container mx-auto px-6 py-4">
    <div class="flex items-center justify-between">
      <a href="/" class="text-xl font-bold">OpenDataLiberia</a>
      
      <div class="hidden md:flex space-x-6">
        <a href="#" class="hover:text-gray-300">Home</a>
        <a href="#" class="hover:text-gray-300">Data</a>
        <a href="#" class="hover:text-gray-300">About</a>
        <a href="#" class="hover:text-gray-300">Contact</a>
      </div>

      <button 
        class="md:hidden"
        on:click={() => isMenuOpen = !isMenuOpen}
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
      </button>
    </div>

    {#if isMenuOpen}
      <div class="md:hidden mt-4 space-y-4">
        <a href="#" class="block hover:text-gray-300">Home</a>
        <a href="#" class="block hover:text-gray-300">Data</a>
        <a href="#" class="block hover:text-gray-300">About</a>
        <a href="#" class="block hover:text-gray-300">Contact</a>
      </div>
    {/if}
  </nav>
</header>
