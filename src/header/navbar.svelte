<script>
  let navbarItems = [
    {
      name: "Home"
    },
    {
      name: "About"
    },
    {
      name: "Services"
    },
    {
      name: "Contact"
    }
  ];

  window.addEventListener("scroll", () => {
    const navbar = document.querySelector(".navbar__wrapper");
    if (window.scrollY > 60) {
      if (!navbar.classList.contains("navbar__wrapper--fixed"))
        navbar.classList.add("navbar__wrapper--fixed");
    } else {
      if (navbar.classList.contains("navbar__wrapper--fixed"))
        navbar.classList.remove("navbar__wrapper--fixed");
    }
  });
</script>

<style>
  .navbar__wrapper {
    width: 100%;
    border-bottom: 2px solid var(--light-gray);
    background-color: #ffffffaa;
  }

  :global(.navbar__wrapper.navbar__wrapper--fixed) {
    position: fixed;
    top: 0;
    background-color: white !important;
  }

  .navbar {
    padding: 1.5em;
    display: flex;
    justify-content: space-between;
    max-width: 1200px;
    margin: 0 auto;
    align-items: center;
  }

  .navbar__list {
    flex-grow: 1;
    display: flex;
    justify-content: space-evenly;
  }

  .navbar__list--item a {
    font-size: 1.2rem;
    font-weight: 600;
    color: var(--gray);
    transition: all 0.3s;
  }

  .navbar__list--item a:hover {
    color: var(--primary-color);
  }

  .navbar__cta {
    font-size: 0.8rem;
    font-weight: 700;
    text-transform: uppercase;
    background-color: var(--secondary-color);
    padding: 2em 3rem;
    transition: all 0.3s;
  }

  .navbar__cta:hover {
    cursor: pointer;
    background-color: var(--primary-color);
  }
</style>

<div class="navbar__wrapper">
  <div class="navbar">
    <div class="navbar__brand">SDG</div>
    <div class="navbar__list">
      {#each navbarItems as item (item.name)}
        <div class="navbar__list--item">
          <a href="#">{item.name}</a>
        </div>
      {/each}
    </div>
    <div class="navbar__cta">Book Today</div>
  </div>
</div>
