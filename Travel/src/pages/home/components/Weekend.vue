<template>
  <div>
      <div class="title">周末去哪</div>
      <div class="recom-info">
        <ul>
          <li class="recom-info-desc border-bottom" v-for="item of list" :key="item.id">
            <div class="recom-img-wraper">
              <img class="recom-img" :src="item.imgUrl" alt="">
            </div>
            <div class="info-text">
              <h5>{{item.title}}</h5>
              <div class="desc">{{item.desc}}</div>
            </div>
          </li>
        </ul>
      </div>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>
<style lang='stylus' scoped>
  .title
    height: .8rem
    text-indent: .5rem
    background: #eee
    line-height: .8rem
    font-size: .32rem
  .recom-info
    .recom-info-desc
      .recom-img-wraper
        overflow:hidden
        height: 0
        padding-bottom: 39.9%
        .recom-img
            width: 100%
            padding: .2rem
            padding-left: 0
      .info-text
        min-width: 0
        padding-top: .2rem
        padding-left: .8em
        h5
          font-size: .32rem
          font-weight: 600
          padding-bottom: .2rem
          white-space: nowrap
          overflow: hidden
          text-overflow: ellipsis
        .desc
          font-size: .14rem
          white-space: nowrap
          overflow: hidden
          text-overflow: ellipsis
</style>
