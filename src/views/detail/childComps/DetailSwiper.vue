<template>
  <div class="detail-swiper">
    <swiper class="swiper-class">
      <swiper-item v-for="(item, index) in topImages" :key="index">
        <img :src="item" alt="">
      </swiper-item>
    </swiper>
  </div>
</template>

<script>
  import {Swiper, SwiperItem} from 'components/common/swiper/index.js'

  export default {
    name: 'DetailSwiper',
    components: {
      Swiper,
      SwiperItem
    },
    data() {
      return {
        
      }
    },
    props: {
      topImages: {
        type: Array,
        default() {
          return []
        }
      }
    }
  }
</script>

<style scoped>
  .swiper-class {
    height: 300px;
  }
</style>
