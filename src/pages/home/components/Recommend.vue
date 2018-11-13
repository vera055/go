<template>
  <div>
    <div class="title">猜你喜欢</div>
    <ul>
      <li
          class="item border-bottom"
          v-for="item of recommendList"
          :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>
export default{
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1810/22/226c137568f18ac0a3.water.jpg_200x200_81ac3ecf.jpg',
        title: '深圳欢乐谷',
        desc: '狂欢无罪，够胆你就来'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1810/22/226c137568f18ac0a3.water.jpg_200x200_81ac3ecf.jpg',
        title: '深圳欢乐谷',
        desc: '狂欢无罪，够胆你就来'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1810/22/226c137568f18ac0a3.water.jpg_200x200_81ac3ecf.jpg',
        title: '深圳欢乐谷',
        desc: '狂欢无罪，够胆你就来'
      }]
    }
  }
}

</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background-color #eee
    text-indent: .2rem
  ul
    margin-left: .24rem
    .item
      overflow: hidden
      display: flex
      padding: .2rem 0
      height: 2.2rem
      .item-img
        width: 2rem
        height: 2rem
        pddding: .1rem
      .item-info
        flex: 1
        padding: .1rem
        overflow: hidden
        .item-title
          line-height: .44rem
          font-size: .32rem
        .item-desc
          line-height: .4rem
          font-size: .24rem
          color: #f55
          ellipsis()
        .item-button
          line-height: .4rem
          margin-top: .2rem
          background-color: #ff9300
          padding: 0 .15rem
          border-radius: .06rem
          color: #fff
</style>
