<script>
  export let menuOpen;
  export let setMenuOpen;

  const links = [
    { href: "/", label: "Inicio" },
    { href: "/directory", label: "Directorio" },
    { href: "/about", label: "Nosotros" },
    { href: "/contact", label: "Contacto" },
  ];
</script>

<nav class="fixed top-0 left-0 w-full z-50 bg-white dark:bg-gray-900 shadow">
  <div class="flex items-center justify-between p-4 max-w-3xl mx-auto">
    <a href="/" class="flex items-center space-x-2">
      <img src="/logo.png" alt="Chacla Logo" class="h-10 w-10" />
      <span class="text-xl font-bold text-gray-800 dark:text-gray-100"
        >Chacla.pe</span
      >
    </a>
    <button
      class="md:hidden p-2 rounded focus:outline-none"
      on:click={() => setMenuOpen(!menuOpen)}
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
      {#each links as { href, label }}
        <li>
          <a
            {href}
            class="text-gray-700 dark:text-gray-200 hover:text-blue-600 dark:hover:text-blue-400 font-medium"
            >{label}</a
          >
        </li>
      {/each}
    </ul>
  </div>
  {#if menuOpen}
    <ul
      class="md:hidden flex flex-col space-y-2 px-4 pb-4 bg-white dark:bg-gray-900 shadow"
    >
      {#each links as { href, label }}
        <li>
          <a
            {href}
            class="block text-gray-700 dark:text-gray-200 hover:text-blue-600 dark:hover:text-blue-400 font-medium"
            on:click={() => setMenuOpen(false)}
          >
            {label}
          </a>
        </li>
      {/each}
    </ul>
  {/if}
</nav>
