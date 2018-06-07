<template>
  <swiper :options="swiperOption" class="wrapper">
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        loop: true,
        autoplay: 2500,
        autoplayDisableOnInteraction: false,
        speed: 500,
        pagination: '.swiper-pagination'
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'https://gw.alicdn.com/tfs/TB1E7_HuHGYBuNjy0FoXXciBFXa-1280-520.jpg_720x720Q75.jpg'
        }, {
          id: '0002',
          imgUrl: 'https://gw.alicdn.com/tfs/TB1HLXNvFOWBuNjy0FiXXXFxVXa-1280-520.jpg_720x720Q75.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background  #ffffff
.wrapper >>> .swiper-pagination-bullet
  width 4px
  height 4px
  border-radius 0
.wrapper
  overflow hidden
  width 100%
  height 0
  padding-bottom 40%
  background #dbdbdb
  .swiper-img
    width 100%
</style>
