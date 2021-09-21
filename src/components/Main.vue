<template>
  <main>
      <div class="main_top">
            <Fumetti 
                v-for="singleJason in dataJason" 
                :key="singleJason.series" 
                :item="singleJason" 
            />    
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
import Fumetti from '@/components/Fumetti.vue'
import MyJson from '@/assets/data/dc-comics.json'

export default {
  name: 'Main',
    components: {
        Fumetti,
    },
  data() {
      return {
          dataJason: MyJson,
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
            ],
        }
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import "../style/generals";
    @import "../style/vars";

    main {
        width: 100%;
        height: 150px;
        background-color: red;
        .main_top {
            width: 100%;
            height: 500px;
            background-color: black;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;
            h1 {
                width: 50%;
                color: white;
                font-size: 25px;
                padding: 50px;
            }
        }
        .main_bottom {
            width: 100%;
            height: 150px;
            background-color: $primary;
            display: flex;
            justify-content: center;
            align-items: center;
            ul {
                width: 80%;
                list-style: none;
                display: flex;
                justify-content: space-around;
                align-items: center;

                li {
                    height: 50px;
                }
                li .img_text_cont {
                    display: flex;
                    align-items: center;
                }
                li .img_text_cont .img_cont {
                    width: 55px;
                    height: 58px;
                }
                li:nth-of-type(4) .img_text_cont .img_cont {
                    width: 45px;
                    height: 65px;
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