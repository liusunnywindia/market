<template>
  <div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide>
      <a class="slideItem">
        <img src="http://gw.alicdn.com/imgextra/i4/188/O1CN01J3HyA21DG8xdo5wIp_!!188-0-lubanu.jpg">
      </a>
    </swiper-slide>
    <swiper-slide>
      <a class="slideItem">
      <img src="https://aecpm.alicdn.com/simba/img/TB15tIjGVXXXXcoapXXSutbFXXX.jpg">
      </a>
    </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper{
    width 100%
    height 140px
    .swiper-container{
      width 100%
      height 100%
      .slideItem{
        width 100%
        height 100%
        display inline-block
        img{
          width 100%
          height 100%
        }
      }
        &>>>.swiper-pagination-bullet{
        background rgb(255, 255, 255)
        opacity 0.3
      }
      &>>>.swiper-pagination-bullet-active {
          opacity: 1;
          background: red;
      }

    }
  }
</style>
