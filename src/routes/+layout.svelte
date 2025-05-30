<script>
  // @ts-nocheck

  import "../app.css";
  import Menu from "$lib/Menu.svelte";
  let menuOpen = false;
</script>

<Menu {menuOpen} setMenuOpen={(v) => (menuOpen = v)} />

<div
  class="bg-gray-100 dark:bg-gray-800 text-gray-900 dark:text-gray-200 min-h-screen flex flex-col items-center pt-20"
>
  <main class="w-full max-w-3xl flex-1 px-4">
    <slot />
  </main>
</div>
