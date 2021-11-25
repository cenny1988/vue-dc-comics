<template>
  <div id="app">
    <Header/>

    <Jumbotron/>
    <main>
      <div class="container">
      </div>
    </main>

    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Jumbotron from './components/Jumbotron.vue';

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Jumbotron,
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
    // debug
    background-color: #000;
    // min-height: 150px;
    color: #fff;
    line-height: 150px;
  }
}
</style>
