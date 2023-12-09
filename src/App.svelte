<script lang="ts">

  import { createEventDispatcher } from 'svelte';

  import MainMenu from './lib/MainMenu.svelte'
  import Library from './lib/Library.svelte'
  import DirectoryContainer from './lib/DirectoryContainer.svelte'
  import Player from './lib/Player.svelte'

  const dispatch = createEventDispatcher();

  export let status = 'idle';

  const updateStatus = (type) => {

    if (status === type) {
      status = 'idle';
    } else {
      status = type
    }

    dispatch('updateStatus', {status})
  }

</script>

<main>
 
  <section>
    
    <article class:undefined="{status === 'idle'}" class:section-left-small={status === 'minimize'} class:section-left-bigger={status === 'maximize'}>

      <MainMenu />
      <Library minimize="{() => updateStatus('minimize')}" maximize="{() => updateStatus('maximize')}" status="{status}" />

    </article>

    <article class:undefined="{status === 'idle'}" class:section-right-bigger={status === 'minimize'} class:section-right-small={status === 'maximize'}>
      <DirectoryContainer />
    </article>
    
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

  main section article:first-child {
    height: 100%;
    width: 420px;
    transition: 0.5s ease all;
  }

  .section-left-small {
    width: 80px !important;
  }

  .section-left-bigger {
    width: 50% !important;
  }

  main section article:last-child {
    height: 100%;
    width: calc(100% - 420px);
    transition: 0.5s ease all;
  }

  .section-right-bigger {
    width: calc(100% - 80px) !important;
  }

  .section-right-small {
    width: 50% !important;
  }

  main section:last-child {
    grid-column: 1 / 3;
    grid-row: 2;
    width: 100%;
    height: 72px;
    position: absolute;
    bottom: 0;
  }

</style>
