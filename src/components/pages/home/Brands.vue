<script setup>
import { SwiperSlide } from 'swiper/vue'
import Slider from '../../Slider.vue'
</script>

<template>
  <div class="brands container">
    <div class="brands-header">
      <h4 class="h4">Бренди</h4>
      <RouterLink class="btn base-btn" to="/"> Дивитися усі </RouterLink>
    </div>
    <hr />
    <div class="brands-list">
      <RouterLink v-for="(item, ind) in 12" :key="ind" to="/"
        ><img src="/Hermossa Logo Beyaz.webp" width="263" height="103" alt="Hermosa"
      /></RouterLink>
    </div>
    <Slider>
      <SwiperSlide><img src="/swiper2/1.jpg" alt="slider1" /></SwiperSlide>
      <SwiperSlide><img src="/swiper2/2.jpg" alt="slider2" /></SwiperSlide>
    </Slider>
  </div>
</template>

<style scoped lang="scss">
.brands {
  margin-block-start: var(--base-block-gap);

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

  &-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(17.875rem, 1fr));
    gap: 1.5rem;
    margin-block-start: 2.5rem;
    margin-block-end: 5rem;

    a {
      display: grid;
      place-items: center;
      padding: 1.75rem 3.125rem;
      border: 0.063rem solid var(--border-primary);

      img {
        transition: transform var(--base-transition);
      }
    }

    @media (hover: hover) {
      a:hover img {
        transform: scale(1.05);
      }
    }
  }
}
</style>
