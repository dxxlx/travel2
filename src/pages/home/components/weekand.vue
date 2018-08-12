<template>
  <div>
    <div class="recommand-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommandList">
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
    data(){
      return{
        recommandList:[{
          id:"0001",
          imgUrl:"http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg",
          title:"华夏文旅海洋公园",
          desc:"华夏文旅海洋公园华夏文旅海洋公园华夏文旅海洋公园华夏文旅海洋公园"
        },{
          id:"0001",
          imgUrl:"http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg",
          title:"华夏文旅海洋公园",
          desc:"华夏文旅海洋公园华夏文旅海洋公园华夏文旅海洋公园华夏文旅海洋公园"
        },{
          id:"0001",
          imgUrl:"http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg",
          title:"华夏文旅海洋公园",
          desc:"华夏文旅海洋公园华夏文旅海洋公园华夏文旅海洋公园华夏文旅海洋公园"
        }]
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
    padding-bottom:33.9%
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
