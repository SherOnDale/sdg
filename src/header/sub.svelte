<script>
  import SubItem from "./sub-item.svelte";
  let items = [
    {
      logo: `
        <svg class="icon icon-phone" viewBox="0 0 32 32">
          <path d="M22 20c-2 2-2 4-4 4s-4-2-6-4-4-4-4-6 2-2 4-4-4-8-6-8-6 6-6 6c0 4 4.109 12.109 8 16s12 8 16 8c0 0 6-4 6-6s-6-8-8-6z"></path>
        </svg>`,
      header: "Address",
      text: "19005 Country Rd.43, Applehill, ON, K0C 1B0"
    },
    {
      logo: `
        <svg class="icon icon-location" viewBox="0 0 32 32">
          <path d="M16 0c-5.523 0-10 4.477-10 10 0 10 10 22 10 22s10-12 10-22c0-5.523-4.477-10-10-10zM16 16.125c-3.383 0-6.125-2.742-6.125-6.125s2.742-6.125 6.125-6.125 6.125 2.742 6.125 6.125-2.742 6.125-6.125 6.125zM12.125 10c0-2.14 1.735-3.875 3.875-3.875s3.875 1.735 3.875 3.875c0 2.14-1.735 3.875-3.875 3.875s-3.875-1.735-3.875-3.875z"></path>
        </svg>`,
      header: "Call Now",
      text: "613-577-8874, 343-370-0390"
    },
    {
      logo: `
        <svg class="icon icon-clock" viewBox="0 0 32 32">
          <path d="M16 0c-8.837 0-16 7.163-16 16s7.163 16 16 16 16-7.163 16-16-7.163-16-16-16zM20.586 23.414l-6.586-6.586v-8.828h4v7.172l5.414 5.414-2.829 2.829z"></path>
        </svg>`,
      header: "Open Hours",
      text: "24 hours a day, 7 days a week"
    }
  ];
</script>

<style>
  .sub-header {
    border-bottom: 2px solid var(--light-gray);
  }

  :global(.icon) {
    display: inline-block;
    width: 1.2rem;
    height: 1.2rem;
    stroke-width: 0;
    stroke: var(--primary-color);
    fill: var(--primary-color);
  }

  .sub-header__wrapper {
    max-width: 1200px;
    margin: 0 auto;
    padding: 1em;
    margin-left: auto;
    height: 60px;
    display: flex;
    justify-content: flex-end;
  }
</style>

<div class="sub-header">
  <div class="sub-header__wrapper">
    {#each items as item (item.header)}
      <SubItem header={item.header} text={item.text} logo={item.logo} />
    {/each}
  </div>
</div>
