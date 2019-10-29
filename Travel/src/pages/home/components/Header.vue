<template>
    <div class="header">
       <div class="header-left">
           <i class="iconfont">&#xe624;</i>
       </div>
       <div class="header-input">
           <i class="iconfont">&#xe632;</i>
           请输入要去的城市
        </div>
       <div class="header-right">
           {{this.city}}
           <i class="iconfont arrow-icon">&#xe6aa;</i>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>
<style lang='stylus' scoped>
    @import '~styles/varibles.styl';
    .header
      display: flex
      line-height: .86rem
      background: $bgColor
      color: #fff
      .header-left
        width: .64rem
        float: left
        text-align: center
        font-size: .4rem
      .header-input
        flex: 1
        height: .62rem
        margin-top: .12rem
        background: #fff
        border-radius: .1rem
        margin-left: .2rem
        color: #ccc
        line-height: .62rem
        padding-left: .1rem
      .header-right
        width: 1.24rem
        float: right
        text-align: center
        .arrow-icon
          margin-left: -.04rem
          vertical-align: middle
</style>
