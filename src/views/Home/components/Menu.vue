<template>
  <div class="iconList">
     <swiper>
      <swiper-slide v-for="(page,index) in pages" :key="index">
        <div class="iconItem" v-for="(item,index) in page" :key="index">
            <a href="" :style="{backgroundImage:'url('+item.imgUrl+')'}">
              <h6>{{item.title}}</h6>
            </a>

        </div>
      </swiper-slide>
     </swiper>
  </div>
</template>
<script>
export default {
  data () {
    return {
    }
  },
  props: {
    list: Array
  },
  methods: {

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
.iconList
   display flex
   flex-wrap wrap
   justify-content center
  .iconItem{
    width 5.6rem
    height 6rem
    float left
    a{
      display inline-block
      background-size: 100% 100%;
      background-repeat: no-repeat;
      width 5.4rem
      height 6rem
      text-direction none
      text-align: center;
      position: relative;
      h6{
        margin 0
        position absolute
        bottom 1rem
        width 100%
        color gray

      }
    }
  }
</style>
