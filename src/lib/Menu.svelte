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

<nav class="navbar bg-base-100 fixed top-0 left-0 w-full z-50 shadow">
  <div class="flex w-full items-center justify-between">
    <div class="navbar-start">
      <a href="/" class="flex items-center space-x-2">
        <img src="/logo.png" alt="Chacla Logo" class="h-10 w-10" />
        <span class="text-xl font-bold"
          >Chacla.pe</span
        >
      </a>
    </div>
    <div class="navbar-end w-auto flex items-center">
      <!-- Desktop menu -->
      <ul class="menu menu-horizontal px-1 hidden md:flex">
        {#each links as { href, label }}
          <li>
            <a {href} class="font-medium">{label}</a>
          </li>
        {/each}
      </ul>
      <!-- Mobile burger -->
      <div class="md:hidden ml-2">
        <button
          class="btn btn-ghost"
          on:click={() => setMenuOpen(!menuOpen)}
          aria-label="Menu"
        >
          <svg
            class="w-6 h-6"
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
      </div>
    </div>
  </div>
  <!-- Mobile dropdown -->
  {#if menuOpen}
    <ul
      class="menu menu-vertical absolute top-full right-4 mt-2 bg-base-100 shadow rounded-box w-48 md:hidden z-50"
    >
      {#each links as { href, label }}
        <li>
          <a {href} on:click={() => setMenuOpen(false)}>{label}</a>
        </li>
      {/each}
    </ul>
  {/if}
</nav>
