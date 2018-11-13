<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li
          class="item border-bottom"
          v-for="item of recommendList"
          :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
          </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>
export default{
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/b9/f9d8ace21c06.jpg_r_640x214_1f239a81.jpg',
        title: '粤东泡汤好去处',
        desc: '全时四季的温泉，度假的天堂'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
        title: '深圳欢乐谷',
        desc: '狂欢无罪，够胆你就来'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1602/88/bf120edeaea383.jpg_r_640x214_f8591f7b.jpg',
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
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.42%
    .item-img
      width: 100%
  .item-info
    flex: 1
    padding: .14rem .2rem .2rem .2rem
    overflow: hidden
    .item-title
      line-height: .44rem
      font-size: .28rem
    .item-desc
      line-height: .4rem
      font-size: .24rem
      color: #616161
      ellipsis()
</style>
