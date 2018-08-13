<template>
  <div>
    <home-header></home-header>
    <home-swiper :swiperList="swiperList"></home-swiper>
    <home-icons :iconList="iconList"></home-icons>
    <home-recommand :recommendList="recommendList"></home-recommand>
    <home-weekand :weekendList="weekendList"></home-weekand>
  </div>
</template>
<script>
  import HomeHeader from './components/Header.vue'
  import HomeSwiper from './components/swiper.vue'
  import HomeIcons from './components/icons.vue'
  import HomeRecommand from './components/recommend.vue'
  import HomeWeekand from './components/weekand.vue'
  import axios from 'axios'
  export default {
    name:'Hello',
    data(){
      return{
        swiperList:[],
        iconList:[],
        recommendList:[],
        weekendList:[]
      }
    },
    components:{
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeRecommand,
      HomeWeekand
    },
    methods:{
      getHomeInfo(){
        axios.get('/api/index.json').then(
          this.getHomeInfoSucc
        )
      },
      getHomeInfoSucc(res){
        res=res.data;
        if(res.ret&&res.data){
          const data=res.data;
          this.swiperList=data.swiperList;
          this.iconList=data.iconList;
          this.recommendList=data.recommendList;
          this.weekendList=data.weekendList;
        }
        console.log(res)
      }
    },
    mounted(){
      this.getHomeInfo()
    }
  }
</script>
<style>
</style>
