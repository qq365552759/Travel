<template>
  <div>
    <div class="tittle">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201312/09/4e2e290c94390948b18fea721f6f15c3.jpg_200x200_ba194523.jpg',
        title: '德萨斯水世界',
        desc: '吴川鼎龙湾德萨斯水世界'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p84/201211/03/3ce0ab9db4b6bbeb93835fbb.jpg_200x200_2b25228d.jpg',
        title: '湖光岩',
        desc: '湖光神秘风情'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1709/51/51589722e6bf272ca3.water.jpg_200x200_0bd1d3c5.jpg',
        title: '湛江红嘴鸥游船',
        desc: '乘风破浪会有时'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .tittle
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
