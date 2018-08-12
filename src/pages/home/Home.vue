<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommand></home-recommand>
    <home-weekand></home-weekand>
  </div>
</template>
<script>
  import HomeHeader from './components/Header.vue'
  import HomeSwiper from './components/swiper.vue'
  import HomeIcons from './components/icons.vue'
  import HomeRecommand from './components/recommend.vue'
  import HomeWeekand from './components/weekand.vue'
  export default {
    name:'Hello',
    components:{
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeRecommand,
      HomeWeekand
    }
  }
</script>
<style>
</style>
