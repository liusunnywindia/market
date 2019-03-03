<template>
  <div class="homeContainer">
    <HomeSwiper></HomeSwiper>
    <Menu :list="menuList"></Menu>
    <Product :list="productList"></Product>
  </div>
</template>
<script>
import HomeSwiper from './components/Swiper'
import Menu from './components/Menu'
import Product from './components/Product'
import axios from 'axios'
export default {
  data () {
    return {
      menuList: [],
      productList: []

    }
  },
  components: {
    HomeSwiper,
    Menu,
    Product
  },
  methods: {
    getList () {
      axios.get('/api/data.json').then(this.getListInfo)
    },
    getListInfo (res) {
      res = res.data[0]
      if (res) {
        this.menuList = res.menuList // 菜单
        this.productList = res.productList
      }
    }
  },
  mounted () {
    this.getList()
  }
}
</script>
<style lang="stylus" scoped>
  .homeContainer{
    display flex
    flex-direction column
  }
</style>
