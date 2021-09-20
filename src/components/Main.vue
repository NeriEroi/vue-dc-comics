<template>
  <main>
      <div class="main_top">
          <h1> - - > Content goes here > - -</h1>
      </div>

      <div class="main_bottom">
          <ul>
              <li v-for="(link, index) in links" :key="index">
                  <div class="img_text_cont">
                      <div class="img_cont">
                          <img :src="require(`../${link.image}`)" alt="link image">
                      </div> 
                      <p>
                          {{ link.text }}
                      </p>
                  </div>
              </li>
          </ul>

      </div>
  </main>
</template>

<script>
export default {
  name: 'Main',

  data() {
      return {
          links: [
              {
                  text: "DIGITAL COMICS",
                  image: "assets/img/buy-comics-digital-comics.png",
              },
              {
                  text: "DC MERCHANDISE",
                  image: "assets/img/buy-comics-merchandise.png",
              },
              {
                  text: "SUBSCRIPTION",
                  image: "assets/img/buy-comics-subscriptions.png",
              },
              {
                  text: "COMIC SHOP LOCATOR",
                  image: "assets/img/buy-comics-shop-locator.png",
              },
              {
                  text: "DC POWER VISA",
                  image: "assets/img/buy-dc-power-visa.svg",
              },
            ]
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import "../style/generals";
    @import "../style/vars";

    main {
        height: 300px;
        background-color: red;
        .main_top {
            height: 150px;
            background-color: black;
            h1 {
                color: white;
                font-size: 25px;
                padding: 50px;
                margin-left: 50px;
            }
        }
        .main_bottom {
            height: 150px;
            background-color: $primary;
            display: flex;
            justify-content: center;
            align-items: center;
            ul {
                list-style: none;
                display: flex;
                justify-content: center;
                align-items: center;

                li {
                    width: 280px;
                    height: 50px;
                }
                li .img_text_cont {
                    display: flex;
                    align-items: center;
                }
                li .img_text_cont .img_cont {
                    width: 55px;
                    height: 60px;
                }
                li .img_text_cont .img_cont img {
                    width: 100%;
                    height: 100%;
                }
                li .img_text_cont p {
                    color: white;
                    padding-left: 10px;
                }
            }
        }
    }

</style>