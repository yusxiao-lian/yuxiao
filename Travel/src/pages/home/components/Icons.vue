<template>
  <div>
    <div class="icons">
      <swiper :options="swiperOption">
        <swiper-slide v-for="(page,index) of pages" :key="index">
          <div class="icon" v-for="item of page" :key="item.id">
            <div class="icon-img">
              <img class="icon-img-content" :src="item.imgUrl" alt="">
            </div>
            <p class="icon-desc">{{item.desc}}</p>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  .icons >>> .swiper-container
    width: 100%
    height: 0
    padding-bottom: 50%
    padding-top: .2rem
  .icon
      position: relative
      float: left
      width: 25%
      height: 0
      overflow: hidden
      padding-bottom: 25%
      .icon-img
        position: absolute
        left: 0
        right: 0
        top: 0
        bottom: .4rem
        box-sizing: border-box
        .icon-img-content
          display: block
          height: 100%
          margin: 0 auto
      .icon-desc
        position: absolute
        bottom: 0
        left: 0
        right: 0
        color: $textColor
        text-align: center
        height: .4rem
        line-height: .4rem
</style>
