<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1508/12/4e6170303c63bdb7070fb1987480afab.water.jpg_600x330_8db91d9d.jpg">
      <div class="banner-info">
        <div class="banner-title">杭州极地海洋世界(AAAA景区)</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe691;</span>39</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201403/07/0a7decf6c090404c1663ab2c88d69189.jpg_r_800x800_1cf71f86.jpg',
        'http://img1.qunarzz.com/sight/p0/201403/07/917f511428a776d712b4a2d3177c392c.jpg_r_800x800_77da4c6c.jpg'
      ]
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0,0,0,0), rgbs(0,0,0,.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0,0,0,.8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
