<template>
  <div>
    <div class="recommand-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of weekendList">
        <div class="item-img-wrappeer">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
  export default {
    name:'HomeWeekand',
    props:{
      weekendList:Array
    },
    data(){
      return{

      }
    }
  }
</script>
<style lang="stylus" scoped>
  @import "~styles/mixin.styl";
  .recommand-title
    line-height:.8rem
    background:#eee;
    text-indent:.2rem;
  .item-img-wrappeer
    height:0
    overflow:hidden
    padding-bottom:37.09%
  .item-img
    width:100%
  .item-info
    padding:.1rem
    min-width:0
    .item-title
      line-height:.54rem
      font-size:.32rem
      font-weight:bold
      ellipsis()
    .item-desc
      line-height:.4rem
      color:#ccc;
      ellipsis()
</style>
