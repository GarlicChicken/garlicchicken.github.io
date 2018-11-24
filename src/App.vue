<template>
  <div id="app">
    <video autoplay loop>
          <source :src="require('./assets/background.mp4')" type="video/mp4">
    </video>
    <Header></Header>
    <Profil></Profil>
    <Portfolio></Portfolio>
    <Footer></Footer>
  </div>
</template>

<script>
  import Header from './components/Header.vue'
  import Footer from './components/Footer.vue'
  import Profil from './components/Profil.vue'
  import Portfolio from './components/Portfolio.vue'

  export default {
    name: 'app',
    data () {
      return {
        
      }
    },
    components: {
      'Header' : Header,
      'Footer' : Footer,
      'Profil' : Profil,
      'Portfolio' : Portfolio
    }
  }
</script>

<style>
  body{
    background-image: url('./assets/background.jpg');
    color: rgb(255, 255, 255);
    font-family: 'Roboto Condensed', sans-serif;
    font-size: 1.1rem;
    cursor:default;
  }
  a{
    cursor: pointer;
    text-decoration: none;
  }
  video {
      position : fixed;
      top : 0; 
      left : 0;
      min-width : 100%;
      min-height : 100%;
      z-index : -1;
      opacity: 0.6;
    }
    ::selection {
      background: rgb(105, 105, 105);
      color: rgb(251, 255, 0);
    }
    ::-moz-selection {
      background: rgb(105, 105, 105);
      color: rgb(251, 255, 0);
    }
</style>
