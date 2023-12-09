<script>

  export let minimize;
  export let maximize;
  export let status;

</script>

<section>

  <nav>
        
    <button class="primary-button" on:click={minimize} title="Contraer tu biblioteca">
      <svg data-encore-id="icon" role="img" aria-hidden="true" viewBox="0 0 24 24" class="Svg-sc-ytk21e-0 iYxpxA"><path d="M3 22a1 1 0 0 1-1-1V3a1 1 0 0 1 2 0v18a1 1 0 0 1-1 1zM15.5 2.134A1 1 0 0 0 14 3v18a1 1 0 0 0 1 1h6a1 1 0 0 0 1-1V6.464a1 1 0 0 0-.5-.866l-6-3.464zM9 2a1 1 0 0 0-1 1v18a1 1 0 1 0 2 0V3a1 1 0 0 0-1-1z"></path></svg>
        <span>Tu biblioteca</span>
    </button>

    <div class="secondary-menu">

      <button title="Crear una lista o carpeta">
        <svg data-encore-id="icon" role="img" aria-hidden="true" viewBox="0 0 16 16" class="Svg-sc-ytk21e-0 kPpCsU"><path d="M15.25 8a.75.75 0 0 1-.75.75H8.75v5.75a.75.75 0 0 1-1.5 0V8.75H1.5a.75.75 0 0 1 0-1.5h5.75V1.5a.75.75 0 0 1 1.5 0v5.75h5.75a.75.75 0 0 1 .75.75z"></path></svg>
      </button>

      <button on:click={maximize} title="Mostrar más">
        <svg class:arrow-active={status === 'maximize'} data-encore-id="icon" role="img" aria-hidden="true" viewBox="0 0 16 16" class="Svg-sc-ytk21e-0 kgVuXA"><path d="M7.19 1A.749.749 0 0 1 8.47.47L16 7.99l-7.53 7.521a.75.75 0 0 1-1.234-.815.75.75 0 0 1 .174-.243l5.72-5.714H.75a.75.75 0 1 1 0-1.498h12.38L7.41 1.529a.749.749 0 0 1-.22-.53z"></path></svg>
      </button>

    </div>

  </nav>

</section>

<style>

  section {
    width: calc(100% - 16px);
    height: calc(100% - 136px);
    background: var(--box-background);
    border-radius: 8px;
    margin: 8px;
    padding: 10px 0;
  }

  nav {
    width: calc(100% - 15px);
    height: 40px;
    padding-right: 20px;
    display: flex;
    justify-content: space-between;
  }

  nav .primary-button {
    text-decoration: none;
    font-weight: 700;
    background: transparent;
    border: none;
    color: var(--text-unactive);
    width: calc(100% - 20px);
    height: 40px;
    display: flex;
    justify-content: left;
    align-items: center;
    padding: 0 20px;
    transition: 0.5s ease all;
  }

  nav .primary-button:hover {
    color: var(--text-active);
  }

  nav .primary-button svg {
    width: 20px;
    margin-right: 15px;
    fill: var(--text-unactive);
    transition: 0.5s ease all;
  }

  nav .primary-button:hover svg {
    fill: var(--text-active);
  }

  .secondary-menu {
    display: flex;
    justify-content: right;
    align-items: center;
  }

  .secondary-menu button {
    width: 30px;
    height: 30px;
    border-radius: 50%;
    margin-left: 10px;
    background: transparent;
    padding: 0;
    border: none;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: 0.5s ease all;
  }

  .secondary-menu button:hover {
    background: var(--button-active);
  }

  .secondary-menu button svg {
    width: 16px;
    height: 16px;
    position: relative;
    fill: var(--text-unactive);
    transform: rotate(0deg);
    transition: 0.5s ease all;
  }

  .arrow-active {
    transform: rotate(180deg) !important;
  }

  .secondary-menu button:hover svg {
    fill: var(--text-active);
  }

</style>
