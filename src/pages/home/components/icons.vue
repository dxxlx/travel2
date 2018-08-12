<template>
  <div class="icons">
    <swiper :options="swiperOption" >
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon"
              v-for="item of page"
             :key="item.id"
        >
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl" alt="">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>

  </div>
</template>
<script>
  export default {
    name:'HomeIcons',
    data(){
      return{
        swiperOption:{
          autoplay:false
        },
        iconList:[{
          id:'0001',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc:'热门景点'
        },{
          id:'0002',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
          desc:'文化古迹'
        },{
          id:'0003',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
          desc:'演出'
        },{
          id:'0004',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          desc:'一日游'
        },{
          id:'0005',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          desc:'西安必游'
        },{
          id:'0006',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          desc:'动植物园'
        },{
          id:'0007',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/95/8d02011d149bdb02.png',
          desc:'汽车票'
        },{
          id:'0008',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
          desc:'逛博物馆'
        },{
          id:'0009',
          imgUrl:'//img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
          desc:'亲子游'

        }]
      }
    },
    computed:{
      pages(){
        const pages=[]
        this.iconList.forEach((item,index)=>{
          const page=Math.floor(index/8)
          if(!pages[page]){
            pages[page]=[]
          }
          pages[page].push(item)
        })
        return pages;
      }
    }
  }
</script>
<style lang="stylus" scoped>
  @import "~styles/varibles.styl";
  @import "~styles/mixin.styl";
  .icons>>> .swiper-container
    height:0;
    padding-bottom:46%;
    padding-top: .1rem;
  .icon
    float:left;
    width:25%;
    height: 1.5rem;
    padding-top: .1rem;
    text-align:center;
    .icon-img
     display:inline-block;
     width:1.1rem;
     height:1.1rem;
     .icon-img-content
      width: 1.1rem;
      height: 1.1rem;
      background: 0;
    .icon-desc
      left:0
      right:0
      bottom:0
      line-height:.44rem
      height:.44rem;
      color:$dartTextColor;
      text-align:center;
      ellipsis()
</style>
