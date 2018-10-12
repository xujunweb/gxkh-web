<template>
    <div>
      <indexHeader></indexHeader>
      <div class="banner">
        <Carousel autoplay v-model="imgindex" loop class="home-banner" :autoplay-speed="speed">
          <CarouselItem>
            <div class="demo-carousel">
              <img src="../../assets/images/banner.png"/>
            </div>
          </CarouselItem>
          <CarouselItem>
            <div class="demo-carousel">
              <img src="../../assets/images/banner.png"/>
            </div>
          </CarouselItem>
          <CarouselItem>
            <div class="demo-carousel">
              <img src="../../assets/images/banner.png"/>
            </div>
          </CarouselItem>
          <CarouselItem>
            <div class="demo-carousel">
              <img src="../../assets/images/banner.png"/>
            </div>
          </CarouselItem>
        </Carousel>
      </div>
      <indexFooter></indexFooter>
    </div>
</template>

<script>
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
      speed:5000
    }
  },
}
</script>

<style>
.banner{
  width: 100%;height: 991px;
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
  height: 991px;position: relative;
}
.ivu-carousel-item{overflow: hidden;}
.demo-carousel{
  width: 1920px;position: relative;left: 50%;margin-left: -960px;
  height: 100%;
}
</style>
