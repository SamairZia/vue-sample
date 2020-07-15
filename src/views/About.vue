<template>
  <div class="about">
    <div class="about-sec-1">
      <div class="container">
        <div class="row">
          <div class="col-sm-12 col-md-6 col-lg-6">
            <h1>About Us</h1>
          </div>
          <div class="col-sm-12 col-md-6 col-lg-6">
            <div class="about-main-right">
              <h4>Our multi-cultural team is made up of over 100 creatives, strategists, analysts and masterminds across our LA, NYC and Europe offices.</h4>
              <p>We have a handful of skeptics that like to challenge our own assumptions and a group of perfectionists that don’t know when to quit. <br>We’re thinkers and innovators who are determined to re-imagine the way we do digital.</p>
            </div>
          </div>
        </div>
        <div class="about-sec-2">
          <carousel :autoplay="true" :nav="false" :loop="true" :items="1" :dots="false">
            <div v-for="( images, index ) in sliderImages" :key="index">
              <img :src="images.img">
            </div>
          </carousel>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import carousel from 'vue-owl-carousel'
export default {
  name: 'About',
  components: { 
    carousel 
  },
  data(){
    return{
      sliderImages: [
        {img: require('@/assets/images/slide1.jpg')},
        {img: require('@/assets/images/slide2.jpg')},
        {img: require('@/assets/images/slide3.jpg')},
      ]
    }
  }
}
</script>

<style scoped>
.about-sec-1{
  padding: 80px 0;
}
.about-sec-1 h1 {
  font-size: 46px;
  font-weight: 800;
  color: #0c0c0c;
  line-height: 1.2;
}
.about-main-right {}
.about-main-right h4 {
  font-size: 30px;
  line-height: 1.3;
  font-weight: 600;
  color: #0c0c0c;
  margin-bottom: 10px;
}
.about-main-right p {
  color: #0c0c0c;
  font-size: 16px;
  line-height: 1.8;
}
.about-sec-2{
  padding: 60px 0;
}
</style>