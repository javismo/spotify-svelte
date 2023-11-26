<script>
  import svelteLogo from './assets/svelte.svg'
  import MainMenu from './lib/MainMenu.svelte'
  import Library from './lib/Library.svelte'
  import Lists from './lib/Lists.svelte'
  import Player from './lib/Player.svelte'
</script>

<main>
 
  <section>
    
    <aside>
      
      <MainMenu />
      
      <Library />

    </aside>

    <aside>
      <!-- <Header /> -->

      <Lists />

    </aside>
    
  </section>

  <section>
    <Player/>
  </section>

</main>

<style>

  main {
    display: flex;
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
  }

  main section {
    width: 100%;
    height: calc(100% - 72px);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  main section aside:first-child {
    height: 100%;
    width: 420px;
  }

  main section aside:last-child {
    height: 100%;
    width: calc(100% - 420px);
  }

  main section:last-child {
    grid-column: 1 / 3;
    grid-row: 2;
    width: 100%;
    height: 72px;
    position: absolute;
    bottom: 0;
  }



  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>
