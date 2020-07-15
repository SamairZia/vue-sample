<template>
  <div class="contact">
    <div class="container">
      <div class="row">
        <div class="col-sm-12 col-md-6 col-lg-6">
          <div class="contact-left-wrap">
            <h3>Get in Touch</h3>
            <p>Creating future-proof digital experiences is what we do. Tell us about your needs, we’d love to collaborate with you.</p>
            <a href="#!">start@samplebrand.com</a>
          </div>
        </div>
        <div class="col-sm-12 col-md-6 col-lg-6">
          <div class="contact-form-wrap">
            <form>
              <div class="req-label">
                <span>*</span>  required fields
              </div>
              <div class="input-wrapper">
                <input type="text" placeholder="Your Name">
                <span>*</span>
              </div>
              <div class="input-wrapper">
                <input type="text" placeholder="Company Name">
                <span>*</span>
              </div>
              <div class="input-wrapper">
                <input type="email" placeholder="Email">
                <span>*</span>
              </div>
              <div class="input-wrapper">
                <input type="text" placeholder="Your Budget">
                <span>*</span>
              </div>
              <div class="input-wrapper">
                <textarea rows="2" placeholder="Describe the project"></textarea>
              </div>
              <button>Submit</button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contact'  
}
</script>

<style scoped>
.contact{
  padding: 80px 0;
}
.contact-left-wrap{

}
.contact-left-wrap h3 {
  font-size: 46px;
  font-weight: 800;
  color: #0c0c0c;
  line-height: 1.2;
}
.contact-left-wrap p {
  color: #0c0c0c;
  font-size: 18px;
  line-height: 1.8;
  margin: 20px 0;
}
.contact-left-wrap a {
  color: #0c0c0c;
  font-size: 22px;
  letter-spacing: 0.4px;
  font-weight: 600;
  padding-bottom: 4px;
  border-bottom: 2px solid #0c0c0c;
  line-height: 1.5;
}
.contact-left-wrap a:hover {
  color: #fc0;
  border-bottom: 2px solid #fc0;
}
.contact-form-wrap{

}
.req-label {
  color: #0c0c0c;
  font-size: 12px;
  text-align: right;
  margin-bottom: 7px;
  margin-right: 20px;
}
.contact-form-wrap span {
  font-size: 30px;
  line-height: 0;
  vertical-align: bottom;
  margin-top: 10px;
  margin-left: 10px;
  color: #0c0c0c8a;
}
.input-wrapper {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
}
.input-wrapper input,.input-wrapper textarea {
  display: block;
  width: 100%;
  height: 45px;
  color: #0c0c0c;
  font-weight: 600;
  font-size: 10px;
  letter-spacing: 4px;
  text-transform: uppercase;
  background-color: rgba(111, 111, 117, .09);
  border: 1px solid transparent;
  line-height: 41px;
  padding: 0 15px;
}
.input-wrapper textarea{
  min-height: 45px;
  height: auto;
}
.input-wrapper span{

}
.contact-form-wrap button {
  display: inline-flex;
  background: #fc0;
  color: #0c0c0c;
  min-width: 200px;
  padding: 15px 0;
  font-size: 14px;
  text-transform: uppercase;
  border: none;
  font-weight: 700;
  line-height: 1;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease-in-out;
}
.contact-form-wrap button:hover {
  background: #0c0c0c;
  border-radius: 4px;
  box-shadow: 3px 3px #fc0;
  color: #fff;
}
</style>