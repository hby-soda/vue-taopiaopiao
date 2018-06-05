<template>
  <div class="header border-bottom">
    <div class="header-left">
      <img class="logo" src="../../../assets/logo.png"/>
      <div class="city">
        西安
        <span class="iconfont city-icon">&#xe6aa;</span>
      </div>
    </div>
    <div class="header-right">
      <div
        class="header-tab"
        :class="{navactive: navactive}"
        @click="handleClickHot"
      >正在热映</div>
      <div
        class="header-tab"
        :class="{navactive: !navactive}"
        @click="handleClickComming"
      >即将上映</div>
      <span class="move pa" :style="{left: moveDistance}"></span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data () {
    return {
      navactive: true,
      moveDistance: '0%'
    }
  },
  methods: {
    handleClickHot () {
      this.navactive = true
      this.moveDistance = '0%'
    },
    handleClickComming () {
      this.navactive = false
      this.moveDistance = '50%'
    }
  }
}
</script>

<style lang="stylus" scoped>
.header
  height .76rem
  .header-left
    float left
    width 3.15rem
    .logo
      display inline-block
      vertical-align middle
      height .50rem
      width .50rem
      padding .12rem .12rem .16rem .36rem
    .city
      display inline-block
      vertical-align middle
      font-size .32rem
      color #999
      .city-icon
        display inline-block
        font-size .12rem
        margin-left -0.06rem
  .header-right
    width: 3.44rem
    float right
    margin-right .91rem
    .header-tab
      display inline-block
      vertical-align middle
      line-height .7rem
      color #777
      text-align center
      padding 0 .28rem
    .navactive
      color #ff4d64
    .move
      display inline-block
      position relative
      bottom .18rem
      width 1.68rem
      border-bottom .06rem solid #ff4d64
      -webkit-transition left 0.7s ease-in-out
      transition left 0.7s ease-in-out
</style>
