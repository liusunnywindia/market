<template>
  <div class="productList">
      <div class="productIem" v-for="(item,index) in list" :key="index">
         <img v-lazy="item.productImg">
         <h6>{{item.productTitle}}</h6>
      </div>
  </div>
</template>
<script>
export default {
  props: {
    list: Array
  },
  data () {
    return {

    }
  }
}
</script>
<style scoped>

</style>
