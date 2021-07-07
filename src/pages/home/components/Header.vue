<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe604;</div>
    </div>
    <div class="header-input">
      <span class="iconfont search-icon">&#xe6a2;</span>
      输入城市/景点游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{ this.city }}
        <span class="iconfont arrow-icon">&#xe6aa;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header
  display: flex
  height: $headerHeight
  line-height: $headerHeight
  text-align: center
  background: $bgColor
  color: #fff
  font-size: .28rem
  .header-left
    float: left
    width: .8rem
    .back-icon
      font-size: .5rem
  .header-input
    flex: 1
    text-align: left
    height: .6rem
    line-height: .6rem
    margin-top: .14rem
    padding-left: .2rem
    border-radius: .06rem
    background: #ffffff
    color: #e4e7ea
  .header-right
    float: right
    min-width: 1.04rem
    padding: 0 .1rem
    text-align: center
    color: #fff
    .arrow-icon
      font-size: .3rem
      margin-left: -.08rem
</style>
