<template>
  <div class="services">
    <h2>Capabilities</h2>
    <div class="services-wrapper">
      <div class="row">
        <div class="col-sm-6 col-md-4 col-lg-4" v-for="(service, index) in services" :key="index">
          <div class="single-service">
            <h3>{{ service.name }}</h3>
            <p> {{ service.desc }} </p>
            <router-link :to="{ path: service.link }" class="view-more">View More</router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Services',
  data() {
    return{
      services: [
        { name: 'Web Design', desc: 'We’re a web design company with deep roots in storytelling. Our award-winning web design team creates custom designs that are human-centered and conversion focused', link: '/services-inner'},
        { name: 'Digital Marketing', desc: 'We create and execute omnichannel digital marketing strategies. From SEO and content to paid search and social, we work with you to capture and convert your target audience.', link: '/services-inner'},
        { name: 'Branding', desc: 'Our branding team creates powerful and holistic brand strategies that set the stage for your marketing initiatives for today and tomorrow.', link: '/services-inner'},
        { name: 'Development', desc: 'Armed with the latest technology, our front and back-end development teams bring your designs to life. We develop for the now and build for the future.', link: '/services-inner'},
        { name: 'Support + Hosting', desc: 'Your digital experience should be: fast, functional and always on. We monitor performance around the clock ensuring full-time uptime and scalability.', link: '/services-inner'}
        
      ]
    }
  }  
}
</script>

<style scoped>
.services{
  padding: 80px 0;
}
.services h2{
  font-weight: 800;
  font-size: 60px;
  line-height: 64px;
  color: #0c0c0c;
  margin-bottom: 30px;
}
.services-wrapper{
 margin-top: 50px; 
}
.single-service{
  padding: 30px 25px;
  transition: all 0.3s ease-in-out;
}
.single-service:hover{
  background: #fc0;
}
.single-service:hover .view-more{
  opacity: 1;
}
.single-service h3 {
  color: #0c0c0c;
  font-size: 34px;
  font-weight: 600;
  line-height: 1.2;
  margin-bottom: 15px;
}
.single-service p {
  color: #0c0c0c;
  font-size: 18px;
  line-height: 1.8;
  margin-bottom: 20px;
}
.view-more {
  display: inline-block;
  color: #0c0c0c;
  font-weight: 600;
  font-size: 24px;
  line-height: 30px;
  border-bottom: 2px solid #0c0c0c;
  opacity: 0;
  transition: all 0.3s ease-in-out;
}
</style>