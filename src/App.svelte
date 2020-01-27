<script>
  import Header from "./header/header.svelte";
</script>

<style>
  :global(:root) {
    --primary-color: #09aeb8;
    --secondary-color: #ffd763;
    --gray: #87868a;
    --light-gray: #f1f1f1;
  }

  :global(a) {
    text-decoration: none;
  }

  :global(a:hover) {
    text-decoration: none;
  }
  :global(*) {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  :global(html) {
    font-size: 16px;
  }

  :global(body) {
    font-family: "Josefin Sans", sans-serif;
    height: 5000px;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }
</style>

<main>
  <Header />
</main>
