<template>
<footer>
  <section id="cards">
      <div class="container">
          <div v-for="card, j in cards" :key="j" class="container-icons">
              <img :src="require(`../assets/img/${card.image}`)" :alt="card.title">
              <h3>{{card.title}}</h3>
          </div>
      </div>
  </section>

  

</footer>
</template>

<script>
export default {
  name: 'Footer',
  data(){
      return{
          cards:[
              {
                  image: 'buy-comics-digital-comics.png',
                  title: 'DIGITAL COMICS'
              },
              {
                  image: 'buy-comics-merchandise.png',
                  title: 'DC MERCHANDISE'
              },
              {
                  image: 'buy-comics-subscriptions.png',
                  title: 'SUBSCRIPTION'
              },
              {
                  image: 'buy-comics-shop-locator.png',
                  title: 'COMIC SHOP LOCATOR'
              },
              {
                  image: 'buy-dc-power-visa.svg',
                  title: 'DC POWER VISA'
              },
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
footer{
    
    #cards{
        background-color: #0282f9;
        
    }
    .container{
        // min-height: 180px;
        padding: 1rem 0;
        display: flex;
        justify-content: space-around;
        align-items: center;
        flex-wrap: wrap;

        .container-icons{
            width: calc(100% / 5);
            padding: 0 20px;
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: space-around;
            // flex-wrap: wrap;
            min-width: 200px;

            img{
                padding: 1rem;
                height: 6rem;
            }
            h3{
                font-size: .7rem;
            }
        }
    }

}
</style>
