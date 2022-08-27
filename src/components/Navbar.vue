<template>
  <div class="nav-bar">
    <nav class="navbar navbar-expand-lg bg-light ">
  <div class="container-fluid pt-2">
    <a class="navbar-brand " href="#"><img src="../assets/Landing/Group 3.svg"></a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse navbar-nav" id="navbarSupportedContent">
        <ul class="ms-lg-auto  navbar-nav">
          <li class="nav-item"><a href="/" class="nav-link login-link">Login</a></li>
          <li class="nav-item"><button class="btn reg-btn">Register</button></li>
        </ul>
    </div>
  </div>
</nav>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.navbar-brand {
  /*margin-left: 2%;*/
  
}

.user-links {

}
.reg-btn {
  
font: normal normal normal 20px/27px Noto Sans;
letter-spacing: 0px;
color: #FFFFFF;
opacity: 1;
background: #01CB63 0% 0% no-repeat padding-box;
box-shadow: 0px 5px 15px #01CB6359;
border-radius: 10px;
opacity: 1;
}

.login-link {
  
font: normal normal bold 20px/27px Noto Sans;
letter-spacing: 0px;
color: #1F2532;
opacity: 1;
}
</style>
