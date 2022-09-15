<template>
  <div>
    <header >
      <b-navbar toggleable="lg" class="px-lg-5">
        <div class="container px-lg-1">
          <b-navbar-brand to="/">
            <img src="~/assets/img/logo.svg" class="" width="190" alt="">
          </b-navbar-brand>

          <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

          <b-collapse id="nav-collapse" is-nav>

            <b-navbar-nav class="mx-auto">

            </b-navbar-nav>


            <b-navbar-nav class="ml-auto">
              <b-nav-item  to="/for-employers" class="mr-3 pr-3 pt-2">Services</b-nav-item>
              <b-nav-item  to="/for-employees" class="mr-3 pt-2">About Us</b-nav-item>
              <b-nav-item  to="/for-employees" class="mr-3 pt-2">Contact Us</b-nav-item>
              <!-- <b-button class="my-2 my-sm-0 btn-secondary mr-lg-4">Contact Us</b-button> -->
              <button  class="btn btn-sacademyy mr-4 ml-4 mt-1" role="button">Login</button>
              <button  class="btn btn-sacademy mt-1" role="button">Register</button>
            </b-navbar-nav>
          </b-collapse>
        </div>
      </b-navbar>
    </header>

  </div>


</template>

<script>
export default{
  name:"header",
  mounted() {
    if (process.client){
      window.onscroll = function () {
        OffSetTop()
      };
    }

    function OffSetTop() {
      if (process.client) {
        let header = document.querySelector(".navbar");
        let sticky = header.offsetTop;
        if (window.pageYOffset > sticky) {
          header.classList.add("sticky");
        } else {
          header.classList.remove("sticky");
        }
      }
    }
  },

}
</script>

<style scoped>


.navbar-light .navbar-nav .nav-link {
  font-family: 'Poppins', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 170%;
  color: #313131;
}

.active {
  color: #E57718;
}

.btn-sacademy {
  background: #20B15A;
  border-radius: 10px;
  color: #fff !important;
  transition: 0.5s;
  border-color:none!important;
  font-size: 15px;
  padding: 12px 15px -9px;
  border-radius: 6px;
  font-family: Poppins;
  font-style: normal;
  font-weight: 500;
  font-size: 15px;
  height: 47px;
}

.btn-sacademyy {
  border-radius: 10px;
  color: #000!important;
  transition: 0.5s;
  border-color: #20B15A!important;
  padding: 0px 25px 0px;
  font-family: Poppins;
  font-style: normal;
  font-weight: 500;
  font-size: 15px;
  height: 47px;
}

.navbar {
  position: fixed;
  -webkit-transition: all .5s ease-in-out;
  -o-transition: all .5s ease-in-out;
  transition: all .5s ease-in-out;
  width: 100%;
  z-index: 1000;
  /*background: #FFF4F4!important;*/

}

.sticky {
  position: fixed;
  top: 0;
  background-color: #fff;
  width: 100%;
  -webkit-transition: all .5s ease-in-out;
  -o-transition: all .5s ease-in-out;
  transition: all .5s ease-in-out;
  -webkit-box-shadow: 0 15px 10px -22px rgba(17, 17, 17, 0.36);
  box-shadow: 0 15px 10px -22px rgba(17, 17, 17, 0.36);
}

.sticky+.content {
  padding-top: 102px;
  -webkit-transition: all .5s ease-in-out;
  -o-transition: all .5s ease-in-out;
  transition: all .5s ease-in-out;
}
</style>
