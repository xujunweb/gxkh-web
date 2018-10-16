<template>
    <div class="footer">
      <div class="footer-content">
        <div class="footer-left">
          <a href="/#/"><img src="../../assets/images/logo.png" class="logo" /></a>
          <div class="companyInfo">
            <p class="comp-phone">联系电话：0755-25320456</p>
            <p class="comp-name">公司名称：深圳市梦宝智能科技有限公司</p>
          </div>
        </div>
        <div class="middle">
          <div class="public">
            <img src="../../assets/images/public.png" />
            <p>微信公众号</p>
          </div>
          <div class="xcxm">
            <img src="../../assets/images/xcxm.jpg" />
          </div>
          <div class="clear"></div>
        </div>
        <div class="footer-right">
          <ul class="footer-list">
            <li class="first-list"><h4>产品</h4></li>
            <li class="list">
              <a href="/#/">经典版</a>
            </li>
            <li class="list">
              <a href="/#/">加大版</a>
            </li>
            <li class="list">
              <a href="/#/">迷你版</a>
            </li>
          </ul>
          <ul class="footer-list">
            <li class="first-list"><h4>商务合作</h4></li>
            <li class="list">
              <a href="/#/">微博</a>
            </li>
            <li class="list">
              <a href="/#/">微信</a>
            </li>
          </ul>
          <ul class="footer-list">
            <li class="first-list"><h4>关于我们</h4></li>
            <li class="list">
              <a href="/#/about">关于我们</a>
            </li>
            <li class="list">
              <a href="/#/">加入我们</a>
            </li>
            <li class="list">
              <a href="/#/">联系我们</a>
            </li>
            <li class="list">
              <a href="/#/">服务协议</a>
            </li>
          </ul>
          <div class="clear"></div>
        </div>
        <div class="clear"></div>
      </div>
    </div>
</template>

<script>
export default {
  name: "indexfooter",
  props: {
    theme: {
      type: String,
      default: 'dark'
    }
  },
  computed:{

  },
  data(){
    return{

    }
  },
  methods:{

  }
}
</script>
<style scoped>
  .footer{width: 100%;padding-top: 50px;background: #fff;padding-bottom: 30px;}
  .footer .footer-content{margin: 0 auto;padding: 0 60px;}
  .footer .footer-left{float: left;}
  .footer .footer-right{float: right;}
  .companyInfo{color: #646464;font-size: 16px;margin-top: 40px;}
  .companyInfo p{margin-bottom: 10px;}
  .footer-list{float: left;margin-left: 70px;color: #2C2C31;}
  .footer-list .first-list{font-size: 16px}
  .footer-list .first-list h4{font-family: '微软雅黑'}
  .footer-list li{margin-bottom: 15px;font-size: 14px;}
  .footer-list li a{color: #646464;}
  .footer-list li a:hover{text-decoration: underline;}
  .middle{float: left;margin-left: 30px;}
  .middle .public{float: left;text-align: center;font-size: 12px;margin-right: 30px;}
  .middle .xcxm{float: left}
  .middle img{float: left;width: 150px;}
</style>
