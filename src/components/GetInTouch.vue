<template>
  <div class="get-touch-sec">
    <div class="container">
      <p>Got a Project or Partnership in Mind?</p>
      <router-link to="/contact" class="get-touch-link">Get In touch</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GetInTouch',
  data(){
    return{
      
    }
  }
}
</script>

<style scoped>
.get-touch-sec{
  background: #fc0;
  padding: 80px 0;
  text-align: center;
  margin-top: 80px;
}
.get-touch-sec p{
  color: #0c0c0c;
  font-size: 18px;
  line-height: 1.5;
  margin-bottom: 15px;
  font-weight: 500;
}
.get-touch-link {
  color: #0c0c0c;
  font-size: 60px;
  line-height: 64px;
  font-weight: 800;
  text-transform: capitalize;
  position: relative;
  z-index: 1;
  padding: 0 4px;
}
.get-touch-link::after {
  content: '';
  width: 100%;
  height: 5px;
  background: #fff;
  position: absolute;
  bottom: 0;
  left: 0;
  z-index: -1;
  transition: all 0.3s ease-in-out;
}
.get-touch-link:hover:after{
  height: 100%;
  z-index: -1;
}
</style>