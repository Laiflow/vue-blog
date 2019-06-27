<template>
 <div id="app">
       <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  
   <Head></Head>

   <router-view></router-view>
   <Footer></Footer>
 </div>
</template>

<script>
import Head from './components/Head.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'app',
  components: {
    Head,
    Footer
  }
}
</script>



<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
@import "https://stackpath.bootstrapcdn.com/bootstrap/4.1.2/css/bootstrap.min.css";
@import "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css";
@import "https://lenpaul.github.io/Lagrange/assets/css/main.css"
</style>