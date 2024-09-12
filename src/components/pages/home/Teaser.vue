<template>
  <div class="teaser">
    <img class="teaser-img" src="/teaser.webp" width="1920" height="1080" alt="Teaser" />
    <div class="overlay" />
    <div class="container">
      <h1 class="h1">ЛОРЕМ ІПСУМ ДОЛОР СІТ АМЕТ</h1>
      <hr />
    </div>
  </div>
</template>

<style scoped lang="scss">
.teaser {
  position: relative;
  height: 100dvh;

  .overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(180deg, rgba(39, 38, 38, 0) 0%, #272626 100%);
  }

  &-img {
    pointer-events: none;
    position: absolute;
    inset: 0;
    object-fit: cover;
    height: 100%;
  }

  .container {
    position: relative;
    display: flex;
    flex-wrap: wrap;
    align-content: flex-end;
    height: 100%;
    padding-block-end: 12vh;

    h1 {
      max-width: 44.688rem;
    }
  }

  hr {
    display: block;
    width: 100%;
    height: 2px;
    margin-block-start: 1rem;
    background-color: var(--content-primary);
  }
}
</style>
