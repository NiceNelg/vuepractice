<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市景点
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.$store.state.city}}
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display flex
    line-height $headerHeight
    background $bgColor
    color #fff
    .header-left 
      width .64rem
      float left
      padding-left .2rem
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      flex 1
      height .64rem
      line-height .64rem
      margin-top .12rem
      margin-left .2rem
      padding-left .2rem
      background #fff
      border-radius .1rem
      color #cccccc
    .header-right 
      width 1.24rem
      float right 
      text-align center
      color #fff
      .arrow-icon
        font-size .2rem
</style>


