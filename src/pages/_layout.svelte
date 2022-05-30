<script>
	import { leftover } from '@roxi/routify';
  import Menu from './_components/Menu.svelte';
  import Navbar from './_components/navbar/Navbar.svelte'
</script>
<div class="layout">
<Menu/>
  <div class="layout-container">
      <div class="nav">
        <Navbar/>
      </div>
      <!-- routify:options preload="proximity" -->
      <slot />
  </div>
</div>
<style>
  .layout {
    display: flex;
  }
  .layout-container {
    flex: 6;
    margin-left: 3.5em;
  }

</style>
