<template>
  <div class="header">
    <router-link to="/">
      <div class="iconfont header-back">&#xe604;</div>
    </router-link>
    城市选择
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header
  position: relative
  height: $headerHeight
  line-height: $headerHeight
  background: $bgColor
  text-align: center
  font-size: .32rem
  color: #fff
  .header-back
    position: absolute
    left: 0
    top: 0
    color: #fff
    width: .8rem
    font-size: .45rem
</style>
