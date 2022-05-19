<script>
  import Menu from './_components/Menu.svelte';
</script>
<div class="menu-container">
  <Menu/>
  <!-- routify:options preload="proximity" -->
  <slot />
</div>
<style>
  .menu-container {
    font-size: 1rem;
    font-weight: 400;
  }
</style>
