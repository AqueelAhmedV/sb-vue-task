<template>
  <div id="app">
    <Navbar />
    <main>
      <!-- Home Section -->
      <section id="home" class="d-flex vh-auto">
        <div class="d-flex p-3 banner-left pt-5">

          <div class="m-auto col-12 col-md-8 col-lg-9 col-xl-10">
            <h1 class="text-white">Anytime, anywhere Learn on your schedule from any device</h1>
            <p class="text-black banner-sub">We Believe everyone has the capacity to be creative <span
                class="text-white">Course Pro</span> is a place where people develop their own potential</p>
            <div class="mt-3">
              <a class="btn bg-black text-white mr-2 pl-3 pt-2 mb-5" href="" role="button">Let's Get Started</a>
            </div>
          </div>
        </div>
        <div class="container-fluid container-fluid-max cover banner-right">

        </div>
      </section>
      <!-- Stats Section -->
      <section class="stats d-flex vh-auto">
        <StatsBar />
      </section>
      <!-- Courses Section -->
      <section>
        <div class="courses mt-5">
          <span class="courses-head d-block">Courses</span>
          <span class="courses-sub">Our Most Popular Courses</span>
          <div class="container-fluid container-fluid-max d-flex justify-content-around" >
            <div class="card mt-3" style="width: 24rem;" v-for="course in courses" v-bind:key="course.id">
              <div class="course-image card-image-top">
                <span class="text-success bg-black course-category p-1 ">{{ course.category }}</span>
              </div>
              <div class="card-body">
                <h5 class="card-title">{{ course.title }}</h5>
                <p class="card-text text-left mr-auto">{{ course.students }} Students</p>
                <div class="d-flex justify-content-between text-secondary pt-3">
                  <span class="duration"><img src="./assets/Landing/schedule-24px.svg"/>{{ course.duration }}</span>
                  <span class="lectures"><img src="./assets/Landing/date_range-24px.svg"/>{{ course.lectures }} Lectures</span>
                </div>
              </div>
              <hr/>
            <div class="card-foot d-flex justify-content-between">
              <div class="course-tutor col-6">
                <img src="https://picsum.photos/40/40/?blur" class="tutor-img"/> 
                <span>{{ course.tutor }}</span>
              </div>
              <div class="course-price col-5 ">  
                <span class="course-newprice text-weight-bold p-1 mb-2">&#8377;{{ course.newprice }}</span>
                <span class="course-oldprice"><strike>&#8377;{{ course.oldprice }}</strike></span>
              </div>
            </div>
            </div>
          </div>
        </div>
      </section>
      <!-- Top Earners Section -->
      <section>...</section>
      <!-- Testimonials Section -->
      <section>...</section>
      <!-- Contact Us Section -->
      <section>
          <span class="courses-head d-block">Courses</span>
          <span class="courses-sub">Our Most Popular Courses</span>
          <div class="container d-flex">
            <div class="container-fluid"></div>
            <div class="container-fluid">
              <FormBox />
            </div>
          </div>
      </section>
    </main>
    <footer>
      
      <div class="container-fluid d-flex card-title justify-content-between pt-3 pb-3 bg-light">
        <span class="container col-4">2021-2022 © Course Pro Private Limited</span>
        <div class="container col-3 d-flex justify-content-between">
          <span><a href="/" class="nav-link ">Terms & Conditions</a></span>
          <span><a href="/" class="nav-link "> Privacy Policy</a></span>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>

import Navbar from "./components/Navbar.vue";
import StatsBar from "./components/StatsBar.vue";
import FormBox from "./components/FormBox.vue";

export default {
  name: "App",
  components: {
    Navbar,
    StatsBar,
    FormBox,
},
  data: function () {
    return {
      courses: [{
        id: 0,
        title: "Ultimate Business Intelligence Analyst A to Z Course 2021",
        category: "Business",
        students: "46,995",
        tutor: "Albert Hitler",
        newprice: 2000,
        oldprice: 2000,
        duration: "11 hr 20 mins",
        lectures: 24
      },
      {
        id: 1,
        title: "Adobe Photoshop Training: From Beginner to Pro",
        category: "Design",
        students: "6,995",
        tutor: "Wanda Wilson",
        newprice: 3000,
        oldprice: 3000,
        duration: "11 hr 20 mins",
        lectures: 24
      },
      {
        id: 2,
        title: "Social Media Marketing - A to Z Content Marketing class 2021",
        category: "Marketing",
        students: "46,995",
        tutor: "Albert Hitler",
        newprice: 2000,
        oldprice: 2000,
        duration: "11 hr 20 mins",
        lectures: 24
      }],
    }
  }
};
</script>

<style>
#app {

  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}



.banner-left {

  text-align: left;
  font: normal normal 50px/70px Noto Sans;
  letter-spacing: 0px;
  color: #FFFFFF;
  text-transform: capitalize;
  opacity: 1;
  background: #01CB63 0% 0% no-repeat padding-box;
}

.banner-left a {
  font: normal normal normal 1.25rem/2.8125rem Noto Sans;
}

.banner-sub {
  font: normal normal normal 1.5625rem/2.8125rem Noto Sans;
}

.banner-sub span {
  font: normal normal bold 1.5625rem/2.8125rem Noto Sans;
}

.banner-left h1 {

  font: normal normal bold 3.4375rem/4.6875rem Noto Sans;
}

.banner-right {

  background-position: top left;
  background-size: cover;
  background-image: url('./assets/Landing/Rectangle 25.svg'), url('./assets/Landing/laptop-g797f7d01f_1920.jpg');
}

hr {
  padding: 0;
  margin: 0;
}

.stats {
  background-image: url('./assets/Landing/Group 12141.svg');
}

.card {
  font-family: Noto Sans;
}

.card-head {
  font-weight: bold;
}

.courses-head {
  color: #01CB63;
  font: normal normal italic 1.4625rem/2.6125rem Noto Sans;
}

.card-title {
  font: normal normal bold 1.2rem/2.3rem Noto Sans;
} 

.courses-sub {
  font: normal normal normal 1.7625rem/3.0rem Noto Sans;
}

.course-image {
  border-radius: inherit;
  position: relative;
  min-height: 30vh;
  background-image: url('https://picsum.photos/200/300/?random');
  background-size: cover;
  background-position: top;
  
}

.card-img-top {
  position: relative;
  
}

.course-category {
  font-family: Noto Sans;
  font-style: normal;
  color: #01CB63;
  border-radius: 4px;
  position: absolute;
  bottom: 5px;
  right: 5px;
}

.course-tutor {
  font: normal normal bold 1rem/2.0rem Noto Sans;

}

.tutor-img {
  clip-path: circle(50%);
  margin: 2%;
}

.course-price {
  margin-top: 2.1vh;
  font: normal normal bold 1rem/2.0rem Noto Sans;
  color: #01CB63;
}

.contact-form .form-field {
  position: relative;
  margin: 32px 0;
}
.contact-form .input-text {
  display: block;
  width: 100%;
  height: 36px;
  border-width: 0 0 2px 0;
  border-color: #5543ca;
  font-size: 18px;
  line-height: 26px;
  font-weight: 400;
}
.contact-form .input-text:focus {
  outline: none;
}
.contact-form .input-text:focus + .label,
.contact-form .input-text.not-empty + .label {
  -webkit-transform: translateY(-24px);
          transform: translateY(-24px);
}
.contact-form .label {
  position: absolute;
  left: 20px;
  bottom: 11px;
  font-size: 18px;
  line-height: 26px;
  font-weight: 400;
  color: #5543ca;
  cursor: text;
  transition: -webkit-transform .2s ease-in-out;
  transition: transform .2s ease-in-out;
  transition: transform .2s ease-in-out, 
  -webkit-transform .2s ease-in-out;
}
.contact-form .submit-btn {
  display: inline-block;
  background-color: #000;
   background-image: linear-gradient(125deg,#a72879,#064497);
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 2px;
  font-size: 16px;
  padding: 8px 16px;
  border: none;
  width:200px;
  cursor: pointer;
}



html {
  font-size: 14px;
}



</style>
