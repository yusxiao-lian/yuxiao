<template>
  <div>
      <div class="title">热门推荐</div>
      <div class="recom-info">
        <ul>
          <li class="recom-info-desc border-bottom" v-for="item of list" :key="item.id">
            <img class="recom-img" :src="item.imgUrl" alt="">
            <div class="info-text">
              <h5>{{item.title}}</h5>
              <div class="desc">{{item.desc}}</div>
              <button class="info-btn">查看详情</button>
            </div>
          </li>
        </ul>
      </div>
  </div>
</template>
<script>
export default {
  name: 'HomeRecom',
  props: {
    list: Array
  }
}
</script>
<style lang='stylus' scoped>
  .title
    height: .8rem
    margin-top: .2rem
    text-indent: .5rem
    background: #eee
    line-height: .8rem
    font-size: .32rem
  .recom-info
    .recom-info-desc
      display: flex
      min-width: 0
      .recom-img
        width: 2rem
        height: 2rem
        padding: .2rem
      .info-text
        flex: 1
        min-width: 0
        padding-top: .2rem
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
        .info-btn
          background: #ffbd1f
          color: #fff
          padding: .02rem
          font-size: .12rem
          border-radius: .1rem
          margin-top: .4rem
</style>
