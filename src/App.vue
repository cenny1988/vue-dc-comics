<template>
  <div id="app">
    <Header/>

    <Jumbotron/>
    <main>
      <div class="container">
        <Carousel/>
      </div>
    </main>

    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Jumbotron from './components/Jumbotron.vue';
import Carousel from '@/components/Carousel.vue';

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Jumbotron,
    Carousel,
  }
}
</script>

<style lang="scss">
#app {
  *{
    margin: 0;
    // padding: 0;
    box-sizing: border-box;
  }
  .container{
    width: 80%;
    margin: 0 auto;
  }

  main{
    background-color: #1c1c1c;
    padding: 2rem 0;
  }
}
</style>
