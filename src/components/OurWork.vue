<template>
  <div class="our-work-sec">
    <h2>Experiences We've <br> Created</h2>
    <div class="work-wrapper">
      <div class="row">
        <div class="col-sm-6 col-md-4 col-lg-4" v-for="(work , index) in works" :key="index">
          <div class="single-work">
            <div class="single-work-img-wrap">
              <img :src="work.image" class="img-fluid" alt="">
              <div class="text">
                <p> {{ work.desc }} </p>
              </div>
            </div>
            <label>{{ work.name }}</label>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'OurWork',
  data() {
    return {
      works: [
        { name: 'Samsung Next', desc: "A single destination to champion what's next in technology and software for backers, entrepreneurs, founders, and builders", image: require('@/assets/images/work-1.jpg') },
        { name: 'Zero Mass Water', desc: "A single destination to champion what's next in technology and software for backers, entrepreneurs, founders, and builders", image: require('@/assets/images/work-2.jpg') },
        { name: 'Citi', desc: "A single destination to champion what's next in technology and software for backers, entrepreneurs, founders, and builders", image: require('@/assets/images/work-3.jpg') },
        { name: 'Optimum', desc: "A single destination to champion what's next in technology and software for backers, entrepreneurs, founders, and builders", image: require('@/assets/images/work-4.jpg') },
        { name: 'a4 Media', desc: "A single destination to champion what's next in technology and software for backers, entrepreneurs, founders, and builders", image: require('@/assets/images/work-5.jpg') },
        { name: 'Dataiku', desc: "A single destination to champion what's next in technology and software for backers, entrepreneurs, founders, and builders", image: require('@/assets/images/work-6.jpg') }
      ]
    }
  }
}
</script>

<style scoped>
  .our-work-sec{
    padding: 80px 0;
  }
  .our-work-sec h2{
    font-weight: 800;
    font-size: 60px;
    line-height: 64px;
    color: #0c0c0c;
    margin-bottom: 30px;
  }
  .work-wrapper{
    margin-top: 40px;
  }
  .single-work{
    margin: 15px;
    cursor: pointer;
  }
  .single-work-img-wrap{
    position: relative;
    margin-bottom: 30px;
  }
  .single-work-img-wrap:hover .text{
    height: 100%;
  }
  .single-work-img-wrap:hover .text p{
    opacity: 1;
  }
  .single-work-img-wrap img{

  }
  .single-work-img-wrap .text{
    position: absolute;
    bottom: 0;
    background: #fc0;
    height: 0;
    display: flex;
    align-items: flex-end;
    transition: all 0.3s ease-in-out;
  }
  .single-work-img-wrap .text p{
    font-size: 18px;
    color: #0c0c0c;
    padding: 35px;
    line-height: 1.5;
    font-weight: 400;
    opacity: 0;
    transition: all 0.3s ease-in-out;
  }
  .single-work label{
    font-size: 24px;
    font-weight: 700;
    line-height: 32px;
    color: #0c0c0c;
    cursor: pointer;
  }

</style>