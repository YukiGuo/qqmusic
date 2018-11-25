<template>
<div id ="header">
        <div class="navOne">
            <div class="nav-left">
                <img src="http://y.gtimg.cn/mediastyle/yqq/img/logo.png?nowebp=1">
                <ul>
                  <li
                  v-for = "(item,index) of list1"
                  :key = index
                  >{{item}}</li>
                </ul>
             </div>
            <div class="nav-right">
                <input type="search" placeholder="搜索音乐、MV、歌单、用户" class="search">
                <span class="login">登录</span>
                <span class="btn1">开通绿钻豪华版</span>
                <span class=" btn2">开通付费包</span>
            </div>
        </div>
        <hr>
        <div class="navTwo">
            <ul>
                <li
                v-for = "(item,index) of list2"
                :key = index
                >{{item}}</li>
            </ul>
        </div>
    </div>
</template>
<script >
export default {
  name: 'Home-Head',
  data: function () {
    return {
      list1: ['音乐馆', '我的音乐', '客户端', '音乐号', 'VIP'],
      list2: ['首页', '歌手', '专辑', '排行榜', '分类歌单', '电台', 'MV', '数字专辑']
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/style/varibles.styl'
#header
  height: 160px
  hr
    margin: 0
  .navOne
    position: relative
    height: 90px
    line-height:90px
    img
      position:absolute
      left:0px
      top:20px
    ul
      position:absolute
      left:200px
      li
        font-size: 18px;
        height: 90px;
        text-align: center;
        display: inline-block;
        line-height: 90px;
        padding: 0 20px;
      li:first-child
        background-color: $bgColor
    .nav-right
      position:absolute
      left:700px
      font-size:14px
      .search
        height:35px
        width: 220px
        border: 1px #cccccc solid
        border-radius: 3px
        padding:0 5px
      .login
        font-size:16px
        margin:0 20px
      .btn1
        background-color:$bgColor
        padding:10px
        border-radius:2px
      .btn2
        padding:8px
        border:solid 1px #ccc
        border-radius:2px
        margin-left:10px
  .navTwo
    text-align:center
    li
      line-height:50px
      display:inline-block
      padding:10px
      font-size:15px
    li:first-child
      color:$bgColor

</style>
