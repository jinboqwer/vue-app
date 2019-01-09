<template>
  <div class="wrapper">
    <swiper :options="swiperOption" ref="mySwiper">
      <!-- slides -->
      <swiper-slide v-for="item of imgList" :key="item.id">
        <img
          class="swiper-img"
          :src="item.url"
          alt="item.id"
        >
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      },
      imgList: [
        {
          id: '1',
          url: "//source.qunarzz.com/site/images/wns/20181227_qunar_homepage_dujia_5.jpg"
        },
        {
          id: '2',
          url: "//source.qunarzz.com/site/images/wns/20190104_dujia_homepage_top_banner_1.jpg"
        },
        {
          id: '3',
          url: "//source.qunarzz.com/site/images/wns/20190103_dujia_homepage_3.jpg"
        }
      ]
    };
  },
  // computed: {
  //   swiper() {
  //     return this.$refs.mySwiper.swiper;
  //   }
  // },
  // mounted() {
  //   // current swiper instance
  //   // 然后你就可以使用当前上下文内的swiper对象去做你想做的事了
  //   console.log("this is current swiper instance object", this.swiper);
  //   this.swiper.slideTo(3, 1000, false);
  // }
};
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: #fff
.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 25.6% 
  .swiper-img 
    width: 100%;

</style>