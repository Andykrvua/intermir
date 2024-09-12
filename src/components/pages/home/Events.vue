<template>
  <div class="events container">
    <div class="events-header">
      <h4 class="h4">Заходи</h4>
      <RouterLink class="btn base-btn" to="/"> Дивитися усі </RouterLink>
    </div>
    <hr />
    <div class="events-list">
      <RouterLink class="events-list-item" v-for="(item, ind) in 3" :key="ind" to="/"
        ><img class="events-list-item-img" src="/example.jpg" width="263" height="103" alt="Hermosa" />
        <div class="events-list-item-options">
          <img src="/icon-calendar.svg" width="24" height="24" aria-hidden="true" />
          <time datetime="2024-12-15">May 05, 2023</time>
          <img src="/icon-location.svg" width="24" height="24" aria-hidden="true" />
          <address>Lorem ipsum dolor sit amet consectetur</address>
        </div>
        <h6 class="events-list-item-title">Назва заходу</h6>
        <p class="events-list-item-descr text-3-line">
          Lorem ipsum dolor sit amet consectetur. Tortor duis quis dolor tellus tristique quisque in ut donec. Lacus
          pharetra adipiscing elit amet. ddddddddddd ddddddddddddd dddddddddddd
        </p>
      </RouterLink>
    </div>
  </div>
</template>

<style scoped lang="scss">
.events {
  margin-block-start: var(--base-block-gap);

  &-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  hr {
    width: calc(50% - 0.75rem);
    height: 1px;
    margin-block-start: 0.5rem;
  }

  &-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(17.875rem, 1fr));
    gap: 1.5rem;
    margin-block-start: 2rem;
    margin-block-end: 0.938rem;

    &-item {
      display: flex;
      flex-direction: column;
      padding: 1rem;
      color: var(--content-primary);
      background-color: var(--background-secondary);

      &-img {
        width: 100%;
        height: 284px;
        object-fit: cover;
      }

      &-options {
        display: grid;
        grid-template-columns: 1.5rem 1fr;
        gap: 0.5rem;
        padding-block-start: 1rem;

        time,
        address {
          font-weight: 700;
          color: var(--content-secondary);
        }
      }

      &-title {
        margin-block-start: 1.5rem;
        font-size: 1.5rem;
        line-height: 2rem;
        font-weight: 700;
      }

      &-descr {
        margin-block-start: 1.5rem;
      }
    }
  }
}
</style>
