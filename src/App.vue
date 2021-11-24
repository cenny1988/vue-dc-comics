<template>
  <div id="app">
    <Header/>

    <main>
      <div class="container">
        <h2> -- Content goes here -- </h2>
      </div>
    </main>

    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Footer,
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
