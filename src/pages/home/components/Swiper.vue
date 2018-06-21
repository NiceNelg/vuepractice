<template>
  <div class="wrapper">
    <swiper :options="swiperOption"  ref="mySwiper">
      <!-- slides -->
      <swiper-slide>
        <img class="swiper-img" src="https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/20180614_CPM_WAP_DE10841.jpg">
      </swiper-slide>
      <swiper-slide>
        <img class="swiper-img" src="https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/20180614_CPM_WAP_DE10841.jpg">
      </swiper-slide>
      <swiper-slide>
        <img class="swiper-img" src="https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/20180614_CPM_WAP_DE10841.jpg">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  data() {
    return {
      swiperOption: {
        
      }
    }
  }
};
</script>


<style lang="stylus" scoped>
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 31.25%
    background #eee
    .swiper-img
      width 100%
</style>
