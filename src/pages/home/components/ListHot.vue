<template>
    <div class="list">
      <ul class="list-info">
        <li class="item">
          <div class="item-info border-bottom" v-for="item of list" :key="item.id">
              <img class="m-img" :src="item.imgUrl" />
              <a class="m-info">
                <div class="title">
                  <div class="m-name">{{item.name}}</div>
                  <i class="m-style" v-show="item.styleshow">
                    <i class="hdr">{{item.hdr}}</i>
                    <i class="lbl">{{item.lbl}}</i>
                  </i>
                </div>
                <div class="deta" v-if="item.shownow">
                  观众评分&nbsp;
                  <span class="txt-waring">{{item.score}}</span>
                </div>
                <div class="deta" v-else>
                  <span class="txt-waring">{{item.num}}&nbsp;</span>
                  人想看&nbsp;
                  <span style="color: #eee">|</span>
                  &nbsp;{{item.time}}
                </div>
                <div class="deta">{{item.director}}</div>
                <div class="deta">{{item.actor}}</div>
                <div class="fantastic" v-show="item.hotshow">
                  <i class="hot" :style="item.warningcolor">{{item.hottxt}}</i>
                </div>
              </a>
              <div class="btn-wrap">
                <a
                  v-if="item.buynow"
                  class="tpp-btn"
                  style="background-image: linear-gradient(45deg,#ff7ba0,#ff4d64)"
                >购票</a>
                <a
                  v-else
                  class="tpp-btn"
                  style="background-image: linear-gradient(45deg,#55c2ff,#349cec)"
                >预售</a>
                <div class="btn-txt"> 特惠</div>
              </div>
            </div>
        </li>
      </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeListHot',
  data () {
    return {
      list: [{
        id: '0001',
        imgUrl: 'https://gw.alicdn.com/i3/TB1gr2sf3KTBuNkSne1XXaJoXXa_.jpg_160x160Q30s100.jpg',
        name: '超时空同居',
        styleshow: false,
        shownow: true,
        score: '8.5',
        director: '         导演：苏伦       ',
        actor: '         主演：雷佳音 佟丽娅 陶虹 徐峥        ',
        buynow: true,
        hotshow: true,
        hottxt: '今日最热',
        warningcolor: {color: '#ff4d64'}
      }, {
        id: '0002',
        imgUrl: 'https://gw.alicdn.com/i4/TB1zFl8uCtYBeNjSspaXXaOOFXa_.jpg_160x160Q75.jpg',
        name: '哆啦A梦：大雄的金银岛',
        styleshow: true,
        hdr: '2D',
        lbl: '中国巨幕',
        shownow: true,
        score: '8.2',
        director: '         导演：今井一晓       ',
        actor: '         主演：水田山葵 大原惠美 嘉数由美       ',
        buynow: true,
        hotshow: true,
        hottxt: '一周最热',
        warningcolor: {color: '#fea54c'}
      }, {
        id: '0003',
        imgUrl: 'https://gw.alicdn.com/i3/TB1VY70niOYBuNjSsD4XXbSkFXa_.jpg_160x160Q30s100.jpg',
        name: '侏罗纪世界2',
        styleshow: true,
        hdr: '3D',
        lbl: 'IMAX',
        shownow: false,
        num: 385237,
        time: '下周五上映',
        director: '         导演：胡安·安东尼奥·巴亚纳       ',
        actor: '         主演：克里斯·帕拉特       ',
        buynow: false,
        hotshow: false
      }, {
        id: '0004',
        imgUrl: 'https://gw.alicdn.com/i4/TB1xcwSheySBuNjy1zdXXXPxFXa_.jpg_160x160Q30s100.jpg',
        name: '复仇者联盟3：无限战争',
        styleshow: true,
        hdr: '3D',
        lbl: 'IMAX',
        shownow: true,
        score: '8.8',
        director: '         导演：安东尼·罗素  乔·罗素       ',
        actor: '         主演：小罗伯特·唐尼 克里斯·海姆斯沃斯       ',
        buynow: true,
        hotshow: false
      }, {
        id: '0005',
        imgUrl: 'https://gw.alicdn.com/i4/TB1xcwSheySBuNjy1zdXXXPxFXa_.jpg_160x160Q30s100.jpg',
        name: '复仇者联盟3：无限战争',
        styleshow: true,
        hdr: '3D',
        lbl: 'IMAX',
        shownow: true,
        score: '8.8',
        director: '         导演：安东尼·罗素  乔·罗素       ',
        actor: '         主演：小罗伯特·唐尼 克里斯·海姆斯沃斯       ',
        buynow: true,
        hotshow: false
      }, {
        id: '0006',
        imgUrl: 'https://gw.alicdn.com/i4/TB1xcwSheySBuNjy1zdXXXPxFXa_.jpg_160x160Q30s100.jpg',
        name: '复仇者联盟3：无限战争',
        styleshow: true,
        hdr: '3D',
        lbl: 'IMAX',
        shownow: true,
        score: '8.8',
        director: '         导演：安东尼·罗素  乔·罗素       ',
        actor: '         主演：小罗伯特·唐尼 克里斯·海姆斯沃斯       ',
        buynow: true,
        hotshow: false
      }, {
        id: '0007',
        imgUrl: 'https://gw.alicdn.com/i4/TB1xcwSheySBuNjy1zdXXXPxFXa_.jpg_160x160Q30s100.jpg',
        name: '复仇者联盟3：无限战争',
        styleshow: true,
        hdr: '3D',
        lbl: 'IMAX',
        shownow: true,
        score: '8.8',
        director: '         导演：安东尼·罗素  乔·罗素       ',
        actor: '         主演：小罗伯特·唐尼 克里斯·海姆斯沃斯       ',
        buynow: true,
        hotshow: false
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.item
  position relative
  padding-left .32rem
  background #ffffff
  .item-info
    display flex
    padding .32rem .32rem .32rem 0
    .m-img
      width 1.4rem
      height 2.1rem
    .m-info
      overflow hidden
      flex 1 1 auto
      padding 0 .22rem
      .title
        display flex
        align-items center
        overflow hidden
        max-width 4.7rem
        .m-name
          color #000
          line-height .48rem
          font-size .32rem
          ellipsis()
          display block
          flex 0 1auto
        .m-style
          flex 0 0 auto
          margin-left .08rem
          font-size .24rem
          height .32rem
          line-height .32rem
          text-align center
          color #999
          border-radius .04rem
          border .02rem solid #999
          padding 0
          .hdr
            display inline-block
            color #fff
            background-color #999
            padding 0 .08rem
            max-width 100%
          .lbl
            display inline-block
            color #777
            background-color #ffffff
            margin-left -.06rem
            padding 0 .08rem
            min-width .76rem
      .deta
        color: #777;
        font-size: 13px;
        margin-top: 3px;
        line-height .38rem
        width: auto;
        ellipsis()
        .txt-waring
          color: #fea54c;
          font-size: 14px;
      .fantastic
        height .48rem
        line-height .48rem
        .hot
          font-size .24rem
          height .32rem
          margin-right .08rem
          padding 0 .08rem
          border .02rem solid
          border-radius .04rem
          min-width 1.12rem
    .btn-wrap
      display flex
      flex 0 0 auto
      flex-direction column
      align-items center
      justify-content center
      .tpp-btn
        border 0
        display inline-block
        text-align center
        vertical-align middle
        user-select none
        color #fff
        background-color transparent
        box-sizing border-box
        height .56rem
        line-height .56rem
        padding 0 .26rem
        font-size .24rem
        border-radius 2.4rem
      .btn-txt
        color #999
        margin-top .11rem
        line-height .36rem
        height .36rem
        font-size .24rem
        ellipsis()
</style>
