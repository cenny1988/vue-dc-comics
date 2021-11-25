<template>
  <div id="app">
    <AppHeader/>

    <Jumbotron/>
    <main>
      <div class="container">
        <Carousel/>
      </div>
    </main>

    <AppFooter/>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import Jumbotron from './components/Jumbotron.vue';
import Carousel from '@/components/Carousel.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
    Jumbotron,
    Carousel,
  }
}
</script>

<style lang="scss">
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
#app {
  .container{
    width: 80%;
    margin: 0 auto;
  }

  main{
    background-color: #1c1c1c;
    padding-bottom: 2rem;
  }

  a{
    color: #fff;
    text-decoration: none;
  }

  // classi btn inserite qui per poterle utilizzare in tutti i componenti
  .button{
    border: #0282f9 1px solid;
    padding: 1rem;

    &.btn-blue{
      background-color: #0282f9;
    }
  }
}
</style>
