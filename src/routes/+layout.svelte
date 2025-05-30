<script>
  import "../app.css";
  let menuOpen = false;
</script>

<div
  class="min-h-screen bg-gray-100 dark:bg-gray-800 text-gray-900 dark:text-gray-200"
>
  <nav
    class="flex items-center justify-between p-4 bg-white dark:bg-gray-900 shadow"
  >
    <div class="flex items-center space-x-2">
      <a href="/" class="flex items-center space-x-2">
        <img src="/logo.png" alt="Chacla Logo" class="h-10 w-10" />
        <span class="text-xl font-bold text-gray-800 dark:text-gray-100"
          >Chacla</span
        >
      </a>
    </div>
    <button
      class="md:hidden p-2 rounded focus:outline-none"
      on:click={() => (menuOpen = !menuOpen)}
      aria-label="Menu"
    >
      <svg
        class="w-6 h-6 text-gray-800 dark:text-gray-100"
        fill="none"
        stroke="currentColor"
        viewBox="0 0 24 24"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M4 6h16M4 12h16M4 18h16"
        />
      </svg>
    </button>
    <ul class="hidden md:flex space-x-6">
      <li>
        <a
          href="/"
          class="text-gray-700 dark:text-gray-200 hover:text-blue-600 dark:hover:text-blue-400 font-medium"
          >Home</a
        >
      </li>
      <li>
        <a
          href="/directory"
          class="text-gray-700 dark:text-gray-200 hover:text-blue-600 dark:hover:text-blue-400 font-medium"
          >Directory</a
        >
      </li>
      <li>
        <a
          href="/about"
          class="text-gray-700 dark:text-gray-200 hover:text-blue-600 dark:hover:text-blue-400 font-medium"
          >About</a
        >
      </li>
      <li>
        <a
          href="/contact"
          class="text-gray-700 dark:text-gray-200 hover:text-blue-600 dark:hover:text-blue-400 font-medium"
          >Contact</a
        >
      </li>
    </ul>
  </nav>

  {#if menuOpen}
    <ul
      class="md:hidden flex flex-col space-y-2 px-4 pb-4 bg-white dark:bg-gray-900 shadow"
    >
      <li>
        <a
          href="/"
          class="block text-gray-700 dark:text-gray-200 hover:text-blue-600 dark:hover:text-blue-400 font-medium"
          >Home</a
        >
      </li>
      <li>
        <a
          href="/directory"
          class="block text-gray-700 dark:text-gray-200 hover:text-blue-600 dark:hover:text-blue-400 font-medium"
          >Directory</a
        >
      </li>
      <li>
        <a
          href="/about"
          class="block text-gray-700 dark:text-gray-200 hover:text-blue-600 dark:hover:text-blue-400 font-medium"
          >About</a
        >
      </li>
      <li>
        <a
          href="/contact"
          class="block text-gray-700 dark:text-gray-200 hover:text-blue-600 dark:hover:text-blue-400 font-medium"
          >Contact</a
        >
      </li>
    </ul>
  {/if}

  <slot />
</div>
