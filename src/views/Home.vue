<template>
  <div class="home">
    <div class="container">
      <div class="main-sec-wrap">
        <h1>Digital Experiences,<br>Re-imagined</h1>
        <p>A full-service digital agency with global capabilities across web design and development, marketing and branding. We create digital experiences that are human-centered and future proof.</p>
      </div>
      <OurWork />
      <div class="text-right mt-4">
        <router-link to="/our-work" class="theme-btn">More Work</router-link>
      </div>
      <Services />
    </div>
    <GetInTouch />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import OurWork from '@/components/OurWork.vue'
import Services from '@/components/Services.vue'
import GetInTouch from '@/components/GetInTouch.vue'

export default {
  name: "Home",
  components: {
    OurWork,
    Services,
    GetInTouch
  }
}
</script>
