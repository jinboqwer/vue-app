<template>
  <div class='header'>
    <div class='header-left'>
      <span class='iconfont icon-fanhui'></span>
    </div>
    <div class='header-input'>
      <span class='iconfont icon-sousuo1'></span>
      输入城市/景点/游玩主题
    </div>
    <div class='header-right'>
      城市
      <span class='iconfont icon-jiantou'></span>
    </div>
  </div>
</template>

<script>



export default {
  name: 'HomeHeader'
  
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/varibles.styl'
  .header
    line-height: .86rem
    display: flex
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .icon-fanhui
        display: block
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      line-height: .64rem
      height: .64rem
      margin-left: .2rem
      margin-top: .12rem
      padding-left: .2rem
      background: #fff
      border-radius: .1rem
      color: #ccc
    .header-right
      width: 1.24rem
      float: right
      text-align: center
      .icon-jiantou
        font-size: .24rem
</style>

