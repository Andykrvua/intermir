<script setup>
import { Navigation, Pagination } from 'swiper/modules'
import { Swiper, SwiperSlide } from 'swiper/vue'

defineProps({
  navigation: Boolean
})

// const props = withDefaults(
//   defineProps({
//     navigation: Boolean
//   }),
//   {
//     navigation: true
//   }
// )

const onSwiper = (swiper) => console.log(swiper)
const onSlideChange = () => console.log('slide change')
</script>

<template>
  <Swiper
    :pagination="{ clickable: true }"
    :navigation="navigation"
    :slides-per-view="1"
    :loop="true"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
    :modules="[Navigation, Pagination]"
  >
    <slot />
  </Swiper>
</template>

<style>
@import 'swiper/css';
@import 'swiper/css/navigation';
@import 'swiper/css/pagination';

.swiper-wrapper {
  margin-block-end: 3.25rem;
}

.swiper-slide {
  text-align: center;
}

.swiper-pagination-bullet {
  width: 0.75rem;
  height: 0.75rem;
  opacity: 1;
  background-color: var(--background-secondary);
}

.swiper-pagination-bullet-active {
  width: 4rem;
  border-radius: 40px;
  background-color: var(--content-primary);
}

.swiper-horizontal > .swiper-pagination-bullets .swiper-pagination-bullet,
.swiper-pagination-horizontal.swiper-pagination-bullets .swiper-pagination-bullet {
  margin: 0 3px;
}

.swiper-button-next::after,
.swiper-button-prev::after {
  content: none;
}

.swiper-button-next,
.swiper-button-prev {
  top: calc(50% - 1.625rem);
  width: 3.5rem;
  height: 3.5rem;
  border-radius: 50%;
  background-color: var(--background-secondary);
  background-position: center;
  background-repeat: no-repeat;
}

.swiper-button-next {
  right: 2.5rem;
  background-image: url('/arrow-right.svg');
}

.swiper-button-prev {
  left: 2.5rem;
  background-image: url('/arrow-left.svg');
}
</style>
