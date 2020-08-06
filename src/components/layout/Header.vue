<template>
  <header>
    <div class="container-fluid">
      <div class="head-wrap">
        <router-link to="/" class="logo-wrap">
          Brand
          <span>name</span>
        </router-link>
        <ul class="main-nav">
          <li :class=" {mainnavdrop : category.isDropFlag, 'dropdow': category.isDropFlag }" class="main-nav-item" v-for="(category, index) in categories" :key="index">
            <router-link :to="{ path: category.link }" class="main-nav-link">{{ category.name }}</router-link>
            <ul class="main-nav-dropdown-menu dropdown-men" v-if="category.isDropFlag">
              <li v-for="(categoryinner, index) in category.child" :key="index">
              <router-link :to="{ path: categoryinner.link }" class="main-nav-dropdown-item"> {{ categoryinner.name }}</router-link>
              </li>
            </ul>
          </li>
          <!--<li class="main-nav-item mainnavdrop dropdow">
            <router-link to="#!" class="main-nav-link">Services</router-link>
            <div class="main-nav-dropdown-menu dropdown-men">
              <router-link to class="main-nav-dropdown-item">Web Design</router-link>
              <router-link to class="main-nav-dropdown-item">Web Development</router-link>
              <router-link to class="main-nav-dropdown-item">Digital Marketing</router-link>
            </div>
          </li>
           <li class="main-nav-item">
            <router-link to="/about" class="main-nav-link">About Us</router-link>
          </li>
          <li class="main-nav-item">
            <router-link to="#!" class="main-nav-link">Blog</router-link>
          </li> -->
        </ul>
        <div class="cta-wrap">
          <router-link to="/contact">Get in touch</router-link>
        </div>
      </div>
    </div>
  </header>
</template> 

<script>
export default {
  name: "Header",
  data() {
    return {
      isDropFlag: false,
      categories: [
        { name: "Latest Work", link: "/about" },
        { 
          isDropFlag: true,
          name: "Services", 
          link: "/services",
          child: [
            { name: "branding", link: "/branding"},
            { name: "Digital Mrketing", link: "/digital"},
            { name: "SEo", link: "/seo"},
          ]
        },
        { name: "About Us", link: "/about-us" },
        { name: "Blog", link: "/blog" }
      ]
    };
  }
};
</script>

<style scoped>
.head-wrap {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 30px;
}
.logo-wrap {
  font-size: 34px;
  color: #0c0c0c;
  text-transform: uppercase;
  font-weight: 700;
  line-height: 1.5;
}
.logo-wrap span {
  color: #fc0;
}
.main-nav {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  flex: 1;
  justify-content: space-evenly;
}
.main-nav-item {
  padding-right: 100px;
  position: relative;
}
.main-nav-link {
  color: #0c0c0c;
  font-size: 15px;
  font-weight: 600;
  line-height: 1.2;
  text-transform: uppercase;
}
.cta-wrap {
}
.cta-wrap a {
  display: inline-flex;
  background: #0c0c0c;
  color: #fff;
  min-width: 200px;
  padding: 15px 0;
  font-size: 14px;
  text-transform: uppercase;
  font-weight: 700;
  line-height: 1;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease-in-out;
}
.cta-wrap a:hover {
  background: #fc0;
  border-radius: 4px;
  box-shadow: 3px 3px #0c0c0c;
  color: #0c0c0c;
}
.mainnavdrop::after {
  content: "";
  height: 7px;
  width: 7px;
  display: inline-block;
  margin-left: 10px;
  border-top: 2px solid #0c0c0c;
  border-right: 2px solid #0c0c0c;
  transform: rotate(135deg);
  position: absolute;
  top: 6px;
  transition: all 0.3s ease-in-out;
}
.mainnavdrop:hover > .main-nav-dropdown-menu {
  display: block;
}
.mainnavdrop:hover .main-nav-link {
  color: #fff;
  position: sticky;
  z-index: 1;
}
.mainnavdrop:hover::after {
  border-color: #fff;
  transform: rotate(-45deg);
  margin-top: 4px;
}
.main-nav-dropdown-menu {
  display: none;
  position: absolute;
  min-width: 180px;
  top: -10px;
  left: -20px;
  box-shadow: 0 0 20px rgba(2, 2, 2, 0.25);
  background-color: #0c0c0c;
  padding: 43px 20px 5px;
  border-radius: 5px;
  margin-right: 7px;
}
.main-nav-dropdown-item {
  color: #fff;
  font-size: 14px;
  line-height: 23px;
  border: solid rgba(255, 255, 255, 0.1);
  border-width: 1px 0;
  padding: 8px 0 9px;
  display: block;
  font-weight: 600;
  text-transform: uppercase;
}
</style>