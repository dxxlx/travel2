<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>

</template>
<script>
  export default {
    name:"HomeSwiper",
    data(){
      return{
        swiperOption:{
          pagination:'.swiper-pagination',
          loop:true,
          autoplay:3000
        },
        swiperList:[{
          id:'0001',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1806/8f/d09fa241a01ac02.jpg_750x200_e0c86013.jpg'
        },{
          id:'0002',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1808/5e/514ce60160e62602.jpg_750x200_9b0074e2.jpg'
        }]
      }
    }
  }
</script>
<style lang="stylus" scoped>
  .wrapper>>> .swiper-pagination-bullet-active
    background #fff !important
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 26.25%
    background-color #eee
    .swiper-img
      width 100%
</style>
