<template>
  <div>
    <detail-banner
      :bannerImg="bannerImg"
      :gallaryImgs="gallaryImgs"
      :sightName="sightName"
    >
    </detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner';
import DetailHeader from './components/Header';
import DetailList from './components/List';

import axios from 'axios';

export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data() {
    return {
      list: [],
      bannerImg: '',
      gallaryImgs: [],
      sightName: ''
    }
  },
  mounted() {
    axios.get('/api/detail.json', {
      params: {
        id: this.$route.params.id
      }
    }).then(this.handleGetDataSucc);
  },
  methods: {
    handleGetDataSucc(res) {
      if( res.data.ret ) {
        const data = res.data.data;
        this.list = data.categoryList;
        this.bannerImg = data.bannerImg;
        this.gallaryImgs = data.gallaryImgs;
        this.sightName = data.sightName;
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .content
      height 50rem
</style>

