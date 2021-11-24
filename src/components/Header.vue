<template>
  <header>
      <div class="container">
          <div id="logo">
              <img src="../assets/img/dc-logo.png" alt="logo-dc">
          </div>
          <nav>
              <ul>
                  <li><a href="#">CHARACTERS</a></li>
                  <li class="active"><a href="#">COMICS</a></li>
                  <li><a href="#">MOVIES</a></li>
              </ul>
          </nav>
      </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
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
            max-height: 100%;

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