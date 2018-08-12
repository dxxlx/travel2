<template>
  <div>
    <div class="recommand-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommandList">
        <img class="item-img" :src="item.imgUrl" alt="">
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
    name:'HomeRecommad',
    data(){
      return{
        recommandList:[{
          id:"0001",
          imgUrl:"http://img1.qunarzz.com/sight/p0/1804/51/512ff9f3a6e9b1a6a3.water.jpg_200x200_f7123f52.jpg",
          title:"华夏文旅海洋公园",
          desc:"华夏文旅海洋公园华夏文旅海洋公园华夏文旅海洋公园华夏文旅海洋公园"
        },{
          id:"0001",
          imgUrl:"http://img1.qunarzz.com/sight/p0/1804/51/512ff9f3a6e9b1a6a3.water.jpg_200x200_f7123f52.jpg",
          title:"华夏文旅海洋公园",
          desc:"华夏文旅海洋公园华夏文旅海洋公园华夏文旅海洋公园华夏文旅海洋公园"
        },{
          id:"0001",
          imgUrl:"http://img1.qunarzz.com/sight/p0/1804/51/512ff9f3a6e9b1a6a3.water.jpg_200x200_f7123f52.jpg",
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
  .item
    display:flex;
    height:1.9rem;
    overflow:hidden
    .item-img
      width:1.7rem;
      height:1.7rem;
      padding:.1rem;
    .item-info
      flex:1
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
      .item-button
        background:#ff9300
        padding: 0 .2rem
        border-radius:.06rem
        margin-top:.16rem
        line-height:.44rem
        color:#fff
</style>
