<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <!-- slides -->
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper" :src="item.imgUrl">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HeaderSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
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
  .wrapper >>> .swiper-pagination-bullet-active  // 进行穿透 这样.wrapper下的组件也能生效了
      background: #fff
  .wrapper >>> .swiper-pagination-bullets
      bottom: .06rem
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom:31.25%;  //图片宽高比
    background: #eee
    .swiper
      width: 100%
</style>
