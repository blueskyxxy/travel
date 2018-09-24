<template>
  <div class="search">
    <input type="text" class="search-input" placeholder="请输入城市名或拼音">
  </div>
</template>

<script>

export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .search
    height: .72rem
    background: $bgColor
    padding: 0 .1rem
    .search-input
      box-sizing: border-box
      width: 100%
      padding: 0 .1rem
      line-height: .64rem
      text-align: center
      background: #fff
      color: #666
</style>
