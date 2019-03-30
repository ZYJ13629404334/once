<template>
<div class="wrapper">
 <swiper :options="swiperOption" >
   <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" alt="">
   </swiper-slide>
   <div class="swiper-pagination" slot="pagination"></div>
 </swiper>
 </div>
</template>
<script>
export default{
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: '//f-flightfe-portalcp.qunarzz.com/f_flightfe_portal_f_flightfe_portal/2019/1553827579640_39399694.jpg'
      }, {
        id: '0002',
        imgUrl: '//f-flightfe-portalcp.qunarzz.com/f_flightfe_portal_f_flightfe_portal/2019/1553827579640_39399694.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
 .wrapper
   width: 100%
   height: 0
   overflow: hidden
   padding-bottom: 31.25%
   background: #eee
   .swiper-img
     width:100%
</style>
