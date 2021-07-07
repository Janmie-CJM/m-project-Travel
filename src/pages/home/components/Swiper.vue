<template>
  <div class="wrapper">
    <swiper :options="swiperOptions" class="wrapper-swiper" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'Homeswiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper /deep/ .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    height: 2.3rem
    overflow: hidden
    width: 100%
    background: #eee
    .wrapper-swiper
      height: 100%
      .swiper-img
        width 100%
</style>
