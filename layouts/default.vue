<template>
  <div>
    <LoadingBar />
    <Header />
    <Nuxt  />
<!--    <Footer />-->
  </div>
</template>

<script>

import Header from "../components/Header";
import LoadingBar from "../components/LoadingBar";
import Footer from "../components/Footer";
export default  {
  components: {Header, Footer, LoadingBar}
}
</script>
