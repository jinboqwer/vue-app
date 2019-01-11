<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgURL" :alt="item.id">
          </div>
          <p class="icon-desc">{{item.imgDesc}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination-icons" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeIcons",

  data() {
    return {
      swiperOption: {
        pagination: {
          el: ".swiper-pagination-icons"
        }
      },
      imgList: [
        {
          id: "001",
          imgURL:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          imgDesc: "热门景点"
        },
        {
          id: "002",
          imgURL:
            "http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png",
          imgDesc: "热门景点"
        },
        {
          id: "003",
          imgURL:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          imgDesc: "热门景点"
        },
        {
          id: "004",
          imgURL:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          imgDesc: "热门景点"
        },
        {
          id: "005",
          imgURL:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          imgDesc: "热门景点"
        },
        {
          id: "006",
          imgURL:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          imgDesc: "热门景点"
        },
        {
          id: "007",
          imgURL:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          imgDesc: "热门景点"
        },
        {
          id: "008",
          imgURL:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          imgDesc: "热门景点热门景点热门景点热门景点"
        },
        {
          id: "009",
          imgURL:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          imgDesc: "热门景点"
        }
      ]
    };
  },
  computed: {
    pages() {
      const pages = [];
      this.imgList.forEach((item, index) => {
        const page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = [];
        }
        pages[page].push(item);
      });
      return pages;
    }
  }
};
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl';
@import '~@/assets/styles/mixins.styl';

.icons >>> .swiper-pagination-icons
  text-align: center
.icons {
  overflow: hidden;
  height: 0;
  padding-bottom: 54%;

  .icon {
    position: relative;
    overflow: hidden;
    float: left;
    width: 25%;
    height: 0;
    padding-bottom: 25%;

    .icon-img {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0.44rem;
      box-sizing: border-box;
      padding-top: 0.1rem;

      .icon-img-content {
        display: block;
        margin: 0 auto;
        height: 100%;
      }
    }

    .icon-desc {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 0.44rem;
      line-height: 0.44rem;
      text-align: center;
      color: $darkTexColor;
      ellipsis();
    }
  }
}
</style>
