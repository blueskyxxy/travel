<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
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
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/28/3e5b3d0e6b72f802.jpg_890x330_c8135dfc.jpg'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/38/b2118fb904e59f02.jpg_890x330_4e350bc5.jpg'
        }
      ]
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
    padding-bottom:37.08%;  //图片宽高比
    background: #eee
    .swiper
      width: 100%
</style>
