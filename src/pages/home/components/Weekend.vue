<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li class="item" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">
            {{item.desc}}
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/p/tts5/1801/a0/333628eebd4f2302.jpg_r_390x260x90_247e4813.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/p/tts5/1801/a0/333628eebd4f2302.jpg_r_390x260x90_247e4813.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/p/tts5/1801/a0/333628eebd4f2302.jpg_r_390x260x90_247e4813.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';
  .title
    margin-top: .2rem
    line-height: .8rem
    background:  #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height : 0
    padding-bottom : 33.9%
  .item-img
    padding: .1rem
  .item-info
    padding : .1rem
    min-width : 0
    .item-title
      ellipsis()
      line-height : .54rem
      font-size : .32rem
    .item-desc
      ellipsis()
      line-height : .4rem
      color : #ccc
</style>
