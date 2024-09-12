<script setup>
import { SwiperSlide } from 'swiper/vue'
import Slider from '../../Slider.vue'
</script>

<template>
  <div class="hero-slider container">
    <div class="hero-slider-header">
      <p class="hero-slider-header-descr subtitle-regular">
        Подорож Hermossa почалася в 2014 році як модний бренд у Туреччині, унікальний у гармонії європейського сучасного
        дизайну з турецькою культурою.
      </p>
      <RouterLink class="btn base-btn" to="/"> Дізнатися більше </RouterLink>
    </div>
    <Slider :navigation="true">
      <SwiperSlide><img src="/swiper1/1.jpg" alt="slider1" /></SwiperSlide>
      <SwiperSlide><img src="/swiper1/2.jpg" alt="slider2" /></SwiperSlide>
      <SwiperSlide><img src="/swiper1/3.jpg" alt="slider3" /></SwiperSlide>
    </Slider>
  </div>
</template>

<style scoped lang="scss">
.hero-slider {
  margin-block-start: var(--base-block-gap);

  &-header {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    margin-block-end: 4rem;

    &-descr {
      max-width: 43.375rem;
    }
  }
}
</style>
