<template>
  <div class="banner" @click="handleBannerClick">
    <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1707/f5/f567cbbff0e26352a3.water.jpg_600x330_5d0a62c0.jpg" />
    <div class="banner-info">
      <div class="banner-tittle">
        渔港公园
      </div>
      <div class="banner-number">
        <span class="iconfont banner-icon">&#xe64a;</span>
        5
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201212/19/3320e43ab4b9cb0493835fbb.jpg_r_800x800_db2deb61.jpg', 'http://img1.qunarzz.com/sight/p0/1606/b7/b71282f8594fa4ebe2.water.jpg_r_800x800_1679d77c.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
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
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-tittle
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
