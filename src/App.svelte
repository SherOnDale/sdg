<script>
  import Header from "./header/header.svelte";
</script>

<style>
  :global(:root) {
    --primary-color: #09aeb8;
  }
  :global(*) {
    box-sizing: border-box;
  }

  :global(html) {
    font-size: 16px;
  }

  :global(body) {
    font-family: "Josefin Sans", sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <Header />
</main>
