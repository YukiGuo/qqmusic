<template>
  <div class="wrapper">
    <h1>歌单推荐</h1>
    <div class="menu">
      <ul>
        <li class="sec1-nav">为你推荐</li>
        <li class="sec1-nav">网络歌曲</li>
        <li class="sec1-nav">经典</li>
        <li class="sec1-nav">夜店</li>
        <li class="sec1-nav">情感</li>
        <li class="sec1-nav">KTV热歌</li>
      </ul>
    </div>
    <div class="listwrapper">
      <ul
      v-for= '(item) of list'
      v-bind:key = item.id
      >
      <!-- <swiper :options="swiperOption" > -->
        <!-- <swiper-slide> -->
          <li class="box"><img :src = item.url><br>
            <span class="title">{{item.title}} </span><br>
            <span class="playnum">播放量： {{item.playNum}}</span>
          </li>
<!--         </swiper-slide>  
        <div class="swiper-pagination"  slot="pagination"></div>
        <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
      </swiper> -->
      </ul>
    </div>
  </div>
</template>

<script >
export default {
  name: 'SongList',
  props: {
    list: Array
  }
  // data: function() {
  //   return{
  //     swiperOption: {}
  //   }
  // }
}
</script>
<style lang="stylus" scoped>
@import '~@/assets/style/varibles.styl'
.wrapper
  padding:30px 0 10px 0
  height:100px
  background-color:#ddd
  h1
    line-height:20px
    font-size:20px
    text-align:center
    margin:auto
  .menu
    text-align:center
    li
      line-height:50px
      display:inline-block
      padding:20px
      font-size:15px
    li:first-child
      color:$bgColor
  .listwrapper
    .box
      width:230px
      float:left
      padding:0 10px
      img
        width:100% 
        padding-bottom:10px 
      .title
      
        line-height:25px
      .playnum 
         font-size:13px
         line-height:25px
         color:#bbb      

</style>
