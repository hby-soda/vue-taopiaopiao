<template>
    <div>
      <home-header @change="handleChange"></home-header>
      <home-swiper v-if="listshow"></home-swiper>
      <home-list-hot v-if="listshow"></home-list-hot>
      <home-list-coming v-else></home-list-coming>
    </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeListHot from './components/ListHot'
import HomeSwiper from './components/Swiper'
import HomeListComing from './components/ListComing'

export default {
  name: 'Home',
  components: {
    HomeListComing,
    HomeSwiper,
    HomeHeader,
    HomeListHot
  },
  data () {
    return {
      listshow: true
    }
  },
  methods: {
    handleChange (mes) {
      this.listshow = mes
    }
  }
}
</script>

<style lang="stylus" scoped>

</style>
