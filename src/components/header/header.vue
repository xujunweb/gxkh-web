<template>
  <div class="header">
    <div class="logo">
      <a href=""><img src="../../assets/images/logo2x.png" /></a>
    </div>
    <div class="tab">
      <a :href="item.herf" v-for="item in tablist" :class="{hover:item.select}">{{item.name}}</a>
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
        {name:'首页',herf:'/',select:false},
        {name:'产品',herf:'/',select:false},
        {name:'商务合作',herf:'/',select:false},
        {name:'关于我们',herf:'/about',select:false},
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
.header .tab a{color: #2C2C31;font-size: 16px;margin-left: 40px;font-weight: bold;display: inline-block;position: relative;}
.header .tab a:hover{color: #E5496E;}
.header .tab a:hover:after{
  content: '';height: 3px;width: 30px;background: #E5496E;
  position: absolute;bottom: -5px;left: 50%;margin-left: -15px;
}
.header .tab a.hover{color: #E5496E;}
.header .tab a.hover:after{
  content: '';height: 3px;width: 30px;background: #E5496E;
  position: absolute;bottom: -5px;left: 50%;margin-left: -15px;
}
</style>
