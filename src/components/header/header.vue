<template>
  <div class="header">
    <div class="logo">
      <a href="/#/"><img src="../../assets/images/logo2x.png" /></a>
    </div>
    <div class="tab">
      <router-link :to="{name:item.herf}" v-for="item in tablist">
        <span :class="{hover:item.select}">{{item.name}}</span>
      </router-link>
    </div>
    <div class="clear"></div>
  </div>
</template>
<script>
export default {
  name: "headerTop",
  props: {
    selectIndex: {
      type: Number,
      default: 0
    }
  },
  computed:{

  },
  data(){
    return{
      tablist:[
        {name:'首页',herf:'home',select:false},
        {name:'产品',herf:'home',select:false},
        {name:'商务合作',herf:'home',select:false},
        {name:'关于我们',herf:'about',select:false},
      ]
    }
  },
  created(){
    this.tablist[this.selectIndex].select = true
  },
  methods:{

  }
}
</script>
<style scoped>
.header{position: absolute;width: 100%;z-index: 2;}
.header .logo{float: left;margin-left: 100px;margin-top: 40px;}
.header .tab{float: right;margin-right: 100px;margin-top: 50px;}
.header .tab span{color: #2C2C31;font-size: 16px;margin-left: 40px;font-weight: bold;display: inline-block;position: relative;cursor: pointer;}
.header .tab span:hover{color: #E5496E;}
.header .tab span:hover:after{
  content: '';height: 3px;width: 30px;background: #E5496E;
  position: absolute;bottom: -5px;left: 50%;margin-left: -15px;
}
.header .tab span.hover{color: #E5496E;}
.header .tab span.hover:after{
  content: '';height: 3px;width: 30px;background: #E5496E;
  position: absolute;bottom: -5px;left: 50%;margin-left: -15px;
}
</style>
