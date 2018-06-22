<template>
  <div class="recommend">
    <scroll ref="scroll" class="recommend-content" :data="discList">
      <div>
        <div class="slider-wrapper">
          <slider>
            <div>
              <a href="http://img1.qunarzz.com/piao/fusion/1801/1a/94428c6dea109402.jpg_640x200_2cf590d8.jpg">
                <img @load="loadImage" src="http://img1.qunarzz.com/piao/fusion/1801/1a/94428c6dea109402.jpg_640x200_2cf590d8.jpg"/>
              </a>
            </div>
            <div>
              <a href="http://img1.qunarzz.com/piao/fusion/1802/42/7c92b9a381e46402.jpg_640x200_1cdce2a4.jpg">
                <img @load="loadImage" src="http://img1.qunarzz.com/piao/fusion/1802/42/7c92b9a381e46402.jpg_640x200_1cdce2a4.jpg"/>
              </a>
            </div>
            <div>
              <a href="http://img1.qunarzz.com/piao/fusion/1802/51/e78f936a5b404102.jpg_640x200_c14f0b3a.jpg">
                <img @load="loadImage" src="http://img1.qunarzz.com/piao/fusion/1802/51/e78f936a5b404102.jpg_640x200_c14f0b3a.jpg"/>
              </a>
            </div>
          </slider>
        </div>

        <div class="recommend-list">
          <h1 class="list-title">热门歌单推荐</h1>
          <ul>
            <li class="item">
              <div class="icon">
                <img @load="loadImage" width="60" height="60" src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_140x140_80f63803.jpg"/>
              </div>
              <div class="text">
                <h2 class="name">name for test name for test name for test name for test name for test name for test</h2>
                <p class="desc">东方宫殿建筑代表，世界宫殿建筑典范</p>
              </div>
            </li>
            <li class="item">
              <div class="icon">
                <img @load="loadImage" width="60" height="60" src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_140x140_80f63803.jpg"/>
              </div>
              <div class="text">
                <h2 class="name">name for test name for test</h2>
                <p class="desc">北京专业级滑雪圣地 北京专业级滑雪圣地 北京专业级滑雪圣地</p>
              </div>
            </li>
            <li class="item">
              <div class="icon">
                <img @load="loadImage" width="60" height="60" src="http://img1.qunarzz.com/sight/p0/1501/f4/f467729126949c3a.water.jpg_140x140_ef235b1c.jpg"/>
              </div>
              <div class="text">
                <h2 class="name">name for test name for test</h2>
                <p class="desc">我爱北京天安门，天安门上太阳升</p>
              </div>
            </li>
            <li class="item">
              <div class="icon">
                <img @load="loadImage" width="60" height="60" src="http://img1.qunarzz.com/sight/p0/1501/f4/f467729126949c3a.water.jpg_140x140_ef235b1c.jpg"/>
              </div>
              <div class="text">
                <h2 class="name">name for test name for test</h2>
                <p class="desc">我爱北京天安门，天安门上太阳升</p>
              </div>
            </li>
            <li class="item">
              <div class="icon">
                <img @load="loadImage" width="60" height="60" src="http://img1.qunarzz.com/sight/p0/1501/f4/f467729126949c3a.water.jpg_140x140_ef235b1c.jpg"/>
              </div>
              <div class="text">
                <h2 class="name">name for test name for test</h2>
                <p class="desc">我爱北京天安门，天安门上太阳升</p>
              </div>
            </li>
            <li class="item">
              <div class="icon">
                <img @load="loadImage" width="60" height="60" src="http://img1.qunarzz.com/sight/p0/1501/f4/f467729126949c3a.water.jpg_140x140_ef235b1c.jpg"/>
              </div>
              <div class="text">
                <h2 class="name">name for test name for test</h2>
                <p class="desc">我爱北京天安门，天安门上太阳升</p>
              </div>
            </li>
            <li class="item">
              <div class="icon">
                <img @load="loadImage" width="60" height="60" src="http://img1.qunarzz.com/sight/p0/1501/f4/f467729126949c3a.water.jpg_140x140_ef235b1c.jpg"/>
              </div>
              <div class="text">
                <h2 class="name">name for test name for test</h2>
                <p class="desc">我爱北京天安门，天安门上太阳升</p>
              </div>
            </li>
            <li class="item">
              <div class="icon">
                <img @load="loadImage" width="60" height="60" src="http://img1.qunarzz.com/sight/p0/1501/f4/f467729126949c3a.water.jpg_140x140_ef235b1c.jpg"/>
              </div>
              <div class="text">
                <h2 class="name">name for test name for test</h2>
                <p class="desc">我爱北京天安门，天安门上太阳升</p>
              </div>
            </li>
            <li class="item">
              <div class="icon">
                <img width="60" @load="loadImage" height="60" src="http://img1.qunarzz.com/sight/p0/1501/f4/f467729126949c3a.water.jpg_140x140_ef235b1c.jpg"/>
              </div>
              <div class="text">
                <h2 class="name">name for test name for test</h2>
                <p class="desc">我爱北京天安门，天安门上太阳升</p>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </scroll>
  </div>
</template>

<script type="text/ecmascript-6">
import Scroll from 'base/scroll/scroll'
import Slider from 'base/slider/slider'
import {getRecommend, getDiscList} from 'api/recommend'
import {ERR_OK} from 'api/config'

export default {
  data() {
    return {
      recommends: [],
      discList: []
    }
  },
  created() {
    this._getRecommend()

    this._getDiscList()
  },
  methods: {
    loadImage() {
      this.$refs.scroll.refresh()
    },
    _getRecommend() {
      getRecommend().then((res) => {
        if (res.code === ERR_OK) {
          this.recommends = res.data.slider
        }
      })
    },
    _getDiscList() {
      getDiscList().then((res) => {
        if (res.code === ERR_OK) {
          this.discList = res.data.list
        }
      })
    }
  },
  components: {
    Slider,
    Scroll
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~common/stylus/variable"

  .recommend
    position: fixed
    width: 100%
    top: 88px
    bottom: 0
    .recommend-content
      height: 100%
      overflow: hidden
      .slider-wrapper
        position: relative
        width: 100%
        overflow: hidden
      .recommend-list
        .list-title
          height: 65px
          line-height: 65px
          text-align: center
          font-size: $font-size-medium
          color: $color-theme
        .item
          display: flex
          box-sizing: border-box
          align-items: center
          padding: 0 20px 20px 20px
          .icon
            flex: 0 0 60px
            width: 60px
            padding-right: 20px
          .text
            display: flex
            flex-direction: column
            justify-content: center
            flex: 1
            line-height: 20px
            overflow: hidden
            font-size: $font-size-medium
            .name
              margin-bottom: 10px
              color: $color-text
            .desc
              color: $color-text-d
      .loading-container
        position: absolute
        width: 100%
        top: 50%
        transform: translateY(-50%)
</style>
