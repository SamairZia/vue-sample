<template>
  <div class="footer">
    <div class="container">
      <div class="row">
        <div class="col-sm-4 col-md-4 col-lg-4">
          <router-link to="/" class="logo-wrap">Brand <span>name</span></router-link>
          <ul class="social-wrap">
              <li><a href="#!"><font-awesome-icon :icon="['fab', 'facebook-f']" /></a></li>
              <li><a href="#!"><font-awesome-icon :icon="['fab', 'instagram']" /></a></li>
              <li><a href="#!"><font-awesome-icon :icon="['fab', 'twitter']" /></a></li>
              <li><a href="#!"><font-awesome-icon :icon="['fab', 'linkedin-in']" /></a></li>
            </ul>
        </div>
        <div class="col-sm-8 col-md-4 col-lg-4 offset-md-4 offset-lg-4">
          <div class="foot-inner-wrap">
            <p>Creating future-proof digital experiences is what we do. Tell us about your needs, we’d love to collaborate with you.</p>
            <a href="#!" class="mail-link">start@samplebrand.com</a>
          </div>
        </div>
      </div>
    </div>
    <div class="foot-bottom">
      <p>Copyright 2020 Sample Brand. All rights reserved.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
.footer{
  background: #0c0c0c;
  padding: 80px 0 0;
}
.foot-inner-wrap{
}
.logo-wrap {
  font-size: 34px;
  color: #fff;
  text-transform: uppercase;
  font-weight: 700;
  line-height: 1.5;
}
.logo-wrap span {
  color: #fc0;
}
.foot-inner-wrap p {
  color: #fff;
  font-size: 18px;
  line-height: 1.5;
  margin-bottom: 15px;
  font-weight: 400;
}
.foot-inner-wrap .mail-link {
  color: #fff;
  font-size: 22px;
  letter-spacing: 0.4px;
  font-weight: 600;
  padding-bottom: 4px;
  border-bottom: 2px solid #fff;
  line-height: 1.5;
}
.foot-inner-wrap .mail-link:hover {
  color: #fc0;
  border-bottom: 2px solid #fc0;
}
.social-wrap{
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  margin-top: 20px;
}
.social-wrap li{
  margin-right: 20px;
}
.social-wrap li a{
  color: #fc0;
  font-size: 20px;
}
.foot-bottom{
  text-align: center;
  padding: 30px 0;
  margin-top: 60px;
  border-top: 1px solid rgba(255,255,255,.07);
}
.foot-bottom p {
  color: #fff;
  font-size: 16px;
  line-height: 1.5;
}
</style>