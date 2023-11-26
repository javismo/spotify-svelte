<script>
  
</script>

<nav>

</nav>

<style>

  nav {
    width: 100%;
    height: 50px;
    background: red;
    position: absolute;
    top: 0;
    left: 0;
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
