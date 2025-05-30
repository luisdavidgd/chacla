<script>
  // @ts-nocheck

  import "../style.css";
  import Menu from "$lib/Menu.svelte";
  let menuOpen = false;
</script>

<Menu {menuOpen} setMenuOpen={(v) => (menuOpen = v)} />

<main class="w-full max-w-3xl flex-1 px-4 mt-32">
  <slot />
</main>

<footer class="w-full max-w-3xl mx-auto py-6 text-center text-sm text-gray-500 dark:text-gray-400">
    © {new Date().getFullYear()} Chacla.pe — Hecho con ❤️ en Chaclacayo
  </footer>
