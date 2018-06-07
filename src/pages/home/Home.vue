<template>
    <div>
      <home-header></home-header>
      <home-swiper></home-swiper>
      <home-list></home-list>
    </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeList from './components/List'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeList
  }
}
</script>

<style lang="stylus" scoped>

</style>
