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

    <section id="footer-nav">
        <div class="container" id="bg-overlay">
            <div id="links">
                <div class="column">
                    <h3>DC COMICS</h3>
                    <ul>
                        <li v-for="link, i in links[0].dcComics" :key="i">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>

                    <h3>SHOP</h3>
                    <ul>
                        <li v-for="link, i in links[1].shops" :key="i">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>
                </div>
                <div class="column">
                    <h3>DC</h3>
                    <ul>
                        <li v-for="link, i in links[2].dc" :key="i">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>
                </div>
                <div class="column">
                    <h3>SITES</h3>
                    <ul>
                        <li v-for="link, i in links[3].sites" :key="i">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="footer-social">
        <div class="container">
            <div>
                <a href="#" class="button">SIGN-UP NOW!</a>
            </div>
            <div>
                <span>FOLLOW US</span>
                <span><a href="#"><img src="../assets/img/footer-facebook.png" alt=""></a></span>
                <span><a href="#"><img src="../assets/img/footer-twitter.png" alt=""></a></span>
                <span><a href="#"><img src="../assets/img/footer-youtube.png" alt=""></a></span>
                <span><a href="#"><img src="../assets/img/footer-pinterest.png" alt=""></a></span>
                <span><a href="#"><img src="../assets/img/footer-periscope.png" alt=""></a></span>
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
          ],
          links:[
              {
                dcComics:['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
              },
              {
                shops:['Shop DC', 'Shop DC Collectibles']
              },
              {
                dc:['Teerms of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertisig', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
              },
              {
                sites:['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
              },
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
footer{
    color: #fff;
    
    a{
        color: #fff;
        text-decoration: none;
    }
    
    #cards{
        background-color: #0282f9;
        
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

    #footer-nav{
        background-image: url('../assets/img/footer-bg.jpg');

        #bg-overlay{
            background-image: url('../assets/img/dc-logo-bg.png');
            background-repeat: no-repeat;
            background-position: right;
            // min-height: 400px;
        }

        #links{
            width: calc(100% / 3);
            padding: 1rem 0;
            display: flex;
            justify-content: space-around;
            padding: 2rem 0;

            .column{
                margin-right: 1rem;
            }
            h3{
                padding: 1rem 0;
            }

            ul{
                padding: 0;
            }
            li{
                list-style: none;
                padding: .2rem 0;
                
                a{
                    color: #959595;
                }
            }
        }
    }

    #footer-social{
        background-color: #303030;

        .container{
            height: 90px;
            display: flex;
            justify-content: space-between;
            align-items: center;

            .button{
                border: #0282f9 1px solid;
                padding: 1rem;
            }

            span{
                color: #0282f9;
                display: inline-block;
                margin: 0 5px;
                height: 40px;
                line-height: 40px;
                vertical-align: middle;
            }
        }
    }

}
</style>
