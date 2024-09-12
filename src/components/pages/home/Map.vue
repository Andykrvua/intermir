<template>
  <div class="map container">
    <div class="map-header">
      <h4 class="h4">Наші клієнти</h4>
    </div>
    <hr />
    <p class="map-descr subtitle-bold">Більше 500 клієнтів по всій Україні</p>
    <img src="/ukraine-map.svg" width="1550" height="1042" alt="Мапа" />
  </div>
</template>

<style scoped lang="scss">
.map {
  margin-block-start: var(--base-block-gap);
  margin-block-end: var(--base-block-gap);

  &-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  hr {
    width: calc(50% - 0.75rem);
    height: 0.063rem;
    margin-block-start: 0.5rem;
  }

  &-descr {
    margin-block-start: 2.5rem;
    margin-block-end: 4.5rem;
  }
}
</style>
