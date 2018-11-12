<template>
  <div>
    <div class="product-top">
      <indexHeader :selectIndex="selectIndex" :showLogo="true" :whitebg="true"></indexHeader>
    </div>
    <div class="product-content">

    </div>
    <indexFooter></indexFooter>
  </div>
</template>

<script>
  import indexFooter from '@/components/footer/footer.vue'
  import indexHeader from '@/components/header/header.vue'
  export default {
    name: "product",
    components:{
      indexFooter,indexHeader,
    },
    data(){
      return{
        selectIndex:1
      }
    },
  }
</script>
<style scoped lang="less">
  .product-top{width: 100%;height: 350px;background: url("../../assets/images/about.png") no-repeat 50% 50%;position: relative;}
</style>
