<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li 
        class="item border-bottom"
        v-for="item in recommendList"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="" />
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
  name: 'HomeWeekend',
  data() {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_140x140_80f63803.jpg',
          title: '大连圣亚海洋世界',
          desc: '第三方士大夫的的方式发多少'
        },
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_140x140_80f63803.jpg',
          title: '大连圣亚海洋世界',
          desc: '第三方士大夫的的方式发多少'
        },
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_140x140_80f63803.jpg',
          title: '大连圣亚海洋世界',
          desc: '第三方士大夫的的方式发多少'
        },
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_140x140_80f63803.jpg',
          title: '大连圣亚海洋世界',
          desc: '第三方士大夫的的方式发多少'
        }
      ]
    }
  }
}
</script>


<style lang="stylus" scoped>
  @import '~styles/mixins.styl';
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .4rem
      font-size .32rem
      elipsis()
    .item-desc
      line-height .4rem
      color #ccc
      elipsis()
</style>
