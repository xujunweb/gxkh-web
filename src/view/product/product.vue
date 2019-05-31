<template>
  <div>
    <div class="product-top">
      <indexHeader :selectIndex="selectIndex" :showLogo="true" :whitebg="true"></indexHeader>
    </div>
    <div class="product-content">
      <div class="vdieo">
        <video src="../../assets/video/course.mp4" controls="controls" height="747.5" width="1300" preload="auto"></video>
      </div>
      <div class="product-list">
        <div class="product-item" v-for="item in productlist">
          <img :src="item.img" @click="handleView(item.img)">
          <p>{{item.title}}</p>
        </div>
      </div>
    </div>
    <indexFooter></indexFooter>
    <Modal title="查看大图" v-model="visible" width="900">
      <img :src="imgName" v-if="visible" style="width: 100%">
    </Modal>
  </div>
</template>

<script>
  import indexFooter from '@/components/footer/footer.vue'
  import indexHeader from '@/components/header/header.vue'
  import productimg from '../../assets/images/productImg.png'
  import productimg2 from '../../assets/images/productImg2.png'
  import productimg3 from '../../assets/images/productImg3.png'
  import productimg4 from '../../assets/images/productImg4.png'
  import productimg5 from '../../assets/images/productImg5.png'
  import productimg6 from '../../assets/images/productImg6.png'
  import { getAllinfo } from  '@/api/user'
  export default {
    name: "product",
    components:{
      indexFooter,indexHeader
    },
    data(){
      return{
        selectIndex:1,
        productlist:[
          {img:productimg,title:'二代智能柜床，折叠状态'},
          {img:productimg2,title:'二代智能柜床，细节展示'},
          {img:productimg3,title:'二代智能柜床，正面尺寸'},
          {img:productimg4,title:'二代智能柜床，全貌'},
          {img:productimg5,title:'二代智能柜床，侧面尺寸'},
          {img:productimg6,title:'二代智能柜床，正面尺寸'}
        ],
        imgName: '',
        visible:false,
      }
    },
    created(){
      this.getAllinfo()
    },
    methods:{
      //查看大图
      handleView (name) {
        this.imgName = name
        this.visible = true
      },
      //获取产品图片
      getAllinfo () {
        getAllinfo().then(res => {
          const data = res.data
          console.log('所有配置',res)
          this.productlist = JSON.parse(data.data[5].value)
        }).catch(err => {
          console.log(err)
        })
      },
    }
  }
</script>
<style scoped lang="less">
  .product-top{width: 100%;height: 162px;position: relative;}
  .product-content{
    background: #F0F4F8;overflow: hidden;
    .vdieo{
      width: 1300px;height: 747.5px;background: #fff;margin: 50px auto;background: #000;
    }
    .product-list{
      display: flex;width: 1300px;margin: 0 auto;flex-wrap: wrap;
      justify-content: space-between;
      .product-item{
        background: #fff;border: 1px solid #DADADA;border-radius: 8px;overflow: hidden;margin-bottom: 50px;
        img{width: 400px;height: 300px;}
        p{line-height: 24px;padding: 15px 0;text-align: center;background: #FAFAFA;color: #333;font-size: 18px;font-weight: 600;}
      }
    }
  }
</style>
