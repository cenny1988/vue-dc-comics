<template>
  <header>
      <div class="container">
          <div id="logo">
              <img src="../assets/img/dc-logo.png" alt="logo-dc">
          </div>
          <nav>
              <ul>
                  <li v-for="link, i in links" :key="i" :class="link.here ? 'active' : '' ">
                      <a  href="#">{{link.text}}</a>
                  </li>
              </ul>
          </nav>
      </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data(){
      return{
          links: [
              {
                  text: "CHARACTERS",
                  url: "#",
                  here: false
              },
              {
                  text: "COMICS",
                  url: "#",
                  here: true
              },
              {
                  text: "MOVIES",
                  url: "#",
                  here: false
              },
              {
                  text: "TV",
                  url: "#",
                  here: false
              },
              {
                  text: "GAMES",
                  url: "#",
                  here: false
              },
              {
                  text: "COLLECTIBLES",
                  url: "#",
                  here: false
              },
              {
                  text: "VIDEOS",
                  url: "#",
                  here: false
              },
              {
                  text: "FANS",
                  url: "#",
                  here: false
              },
              {
                  text: "NEWS",
                  url: "#",
                  here: false
              },
              {
                  text: "SHOP",
                  url: "#",
                  here: false
              },

          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

header{
    background-color: #ffffff;
    height: 100px;

    .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
        max-height: 100%;
    
        #logo>img{
            max-height: 100px;
            padding: 10px 0;
        }
        nav{
            ul{
                display: flex;
                justify-content: space-around;
            }

            li{
                display: inline-block;
                line-height: 77px;
                padding: 10px;
                
                &.active{
                    border-bottom: #0c7cec 3px solid;
                    a{
                        color: #0c7cec;
                    }
                }

                a{
                    text-decoration: none;
                    color: #000;
                }
            }
        }
    }
}

</style>