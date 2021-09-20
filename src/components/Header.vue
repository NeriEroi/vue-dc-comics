<template>
  <header>
      <div class="logo_cont">
          <img src="@/assets/img/dc-logo.png" alt="dc-logo">
      </div>

      <nav>
          <ul>
              <li v-for="(link, index) in links" :key="index" :class="(link.current) ? 'active' : null">
                  {{ link.text }}
              </li>
          </ul>
      </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',

  data() {
      return {
         links: [
             {
                 text: "CHARACTERS",
                 url: "#",
                 current: false,
             },
             {
                 text: "COMICS",
                 url: "#",
                 current: true,
             },
             {
                 text: "MOVIES",
                 url: "#",
                 current: false,
             },
             {
                 text: "TV",
                 url: "#",
                 current: false,
             },
             {
                 text: "GAMES",
                 url: "#",
                 current: false,
             },
             {
                 text: "COLLECTIBLES",
                 url: "#",
                 current: false,
             },
             {
                 text: "VIDEOS",
                 url: "#",
                 current: false,
             },
             {
                 text: "FANS",
                 url: "#",
                 current: false,
             },
             {
                 text: "NEWS",
                 url: "#",
                 current: false,
             },
             {
                 text: "SHOP",
                 url: "#",
                 current: false,
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

    header {
        height: 150px;
        display: flex;
        justify-content: space-around;
        align-items: center;
        .logo_cont {
            width: 70px;
            height: 70px;
            margin-left: 50px;
            img {
                width: 100%;
                height: 100%;
            }
        }
        ul {
            display: flex;
            list-style: none;
            li {
                font-size: 15px;
                font-weight: 600;
                margin-right: 20px;
                text-decoration: none;
                color: black;
                padding-bottom: 50px;

                &.active {
                    color: $primary;
                    border-bottom: 5px solid $primary;
                }
            }
        }
    }
</style>