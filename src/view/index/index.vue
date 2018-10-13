<template>
    <div>
      <div class="banner">
        <indexHeader></indexHeader>
        <Carousel autoplay v-model="imgindex" loop class="home-banner" :autoplay-speed="speed">
          <CarouselItem v-for="item in imglist">
            <div class="demo-carousel">
              <img :src="item.src"/>
            </div>
          </CarouselItem>
        </Carousel>
      </div>
      <indexFooter></indexFooter>
    </div>
</template>

<script>
import imgsrc from  '@/assets/images/banner.png'
import indexFooter from '@/components/footer/footer.vue'
import indexHeader from '@/components/header/header.vue'
export default {
  name: "index",
  components:{
    indexFooter,indexHeader
  },
  data(){
    return{
      imgindex:0,
      speed:5000,
      imglist:[
        {src:imgsrc},
        {src:imgsrc},
        {src:imgsrc},
        {src:imgsrc}
      ]
    }
  },
}
</script>

<style>
.banner{
  width: 100%;height: 600px;position: relative;
}
.ivu-carousel-dots li button{
  background: #fff;
  width: 6px;
  height: 6px;
  opacity: 1;
  border-radius: 50%;
}
.ivu-carousel-dots li.ivu-carousel-active > button{
  background: #E5496E;border-radius: 3px;
  height:6px;
}
.ivu-carousel-dots-inside{bottom:15px;}
.home-banner{
  height: 600px;position: relative;overflow: hidden;
}
.ivu-carousel-item{overflow: hidden;}
.demo-carousel{
  width: 1920px;position: relative;left: 50%;margin-left: -960px;
}
.demo-carousel img{
}
</style>
