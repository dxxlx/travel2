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
    props:{
      iconList:Array
    },
    data(){
      return{
        swiperOption:{
          autoplay:false
        },
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
