<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list="iconList"></home-icons>
    <home-recommend :list="recommendList"></home-recommend>
    <home-weekend :list="weekendList"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header';
import HomeSwiper from './components/Swiper';
import HomeIcons from './components/Icons';
import HomeRecommend from './components/Recommend';
import HomeWeekend from './components/Weekend';
import axios from 'axios';

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  mounted() {
    this.getHomeInfo()
  },
  data() {
    return {
      city: "",
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  methods: {
    getHomeInfo() {
      axios.get('/static/mock/index.json').then(this.getHomeInfoSucc);
    },
    getHomeInfoSucc(result) {
      console.log(result.data.data.swiperList);
      if( result.data.result && result.data.data.city ) {
        this.city = result.data.data.city;
        this.swiperList = result.data.data.swiperList;
        this.iconList = result.data.data.iconList;
        this.recommendList = result.data.data.recommendList;
        this.weekendList = result.data.data.weekendList;
      }
    }
  }
};
</script>
