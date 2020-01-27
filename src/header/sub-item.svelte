<script>
  export let header = "Default Header";
  export let text = "Default Text";
  export let logo = `<svg></svg>`;
</script>

<style>
  .sub-header__item--wrapper {
    margin-right: 0.5rem;
    font-size: 0.9rem;
    display: flex;
    align-items: center;
  }

  .sub-header__item--wrapper div {
    margin-right: 0.5rem;
  }

  .sub-header__item--header {
    font-weight: 600;
  }

  .sub-header__item--text {
    color: var(--gray);
  }
</style>

<div class="sub-header__item--wrapper">
  <div class="logo">
    {@html logo}
  </div>
  <div class="sub-header__item--header">{header}</div>
  <div class="sub-header__item--text">{text}</div>
</div>
