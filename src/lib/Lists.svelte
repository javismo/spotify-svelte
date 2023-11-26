<script>
  import AppHeader from './AppHeader.svelte';
</script>

<main>

  <AppHeader />

  All lists

</main>

<style>

  main {
    width: calc(100% - 10px);
    height: calc(100% - 30px);
    position: relative;
    background: var(--box-background);
    border-radius: 8px;
    margin: 10px 10px 10px 0;
    padding: 10px 0;
    overflow-x: hidden;
  }

  nav ul {
    margin: 0;
    padding: 0;
    list-style: none;
    text-align: left;
  }

  nav ul a {
    text-decoration: none;
    font-weight: 700;
    color: var(--text-unactive);
    width: calc(100% - 20px);
    height: 40px;
    display: flex;
    align-items: center;
    padding: 0 20px;
    transition: 0.5s ease all;
  }

  nav ul a:hover {
    color: var(--text-active);
  }

  nav ul li {
    display: flex;
    justify-content: left;
    align-items: center;
  }

  nav ul li svg {
    width: 20px;
    margin-right: 20px;
    fill: var(--text-unactive);
    transition: 0.5s ease all;
  }

  nav ul a:hover svg {
    fill: var(--text-active);
  }

</style>
