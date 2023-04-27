
<script>
import {headerMenus, DCMenu, shopMenu, sitesMenu} from '../js/all-menus'
export default {
  name: 'Footer',
  data(){
    return{
      headerMenus,
      DCMenu,
      shopMenu,
      sitesMenu
    }
  }
}
</script>

<template>

  <div class="footerTop">
    <div class="container">
        <div class="menus-side">

         <div>
          <ul>
            <h4>DC COMICS</h4>
            <li v-for="(link, index) in headerMenus" :key="index">
              <a :href="link.href">
                {{link.text}}
              </a>
            </li>
          </ul>

          <ul>
            <h4>SHOP</h4>
            <li v-for="(link, index) in shopMenu" :key="index">
              <a :href="link.href">
                {{link.text}}
              </a>
            </li>
          </ul>
         </div>

          <ul>
            <h4>DC</h4>
            <li v-for="(link, index) in DCMenu" :key="index">
              <a :href="link.href">
                {{link.text}}
              </a>
            </li>
          </ul>

          <ul>
            <h4>SITES</h4>
            <li v-for="(link, index) in sitesMenu" :key="index">
              <a :href="link.href">
                {{link.text}}
              </a>
            </li>
          </ul>

        </div>
        <div class="logoSide">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
    </div>
  </div>

  <div class="footerBottom">

  </div>
</template>

<style lang="scss" scoped>
@import '../scss/partials/general';

      .footerTop {
      background-image: url('../assets/img/footer-bg.jpg');
      background-size: cover;
      width: 100%;
      height: 370px;
      overflow: hidden;

      .container{
        display: flex;
        
        .menus-side{
          margin-top: 30px;
          display: flex;
          width: 50%;
          h4{
            color: white;
            margin-bottom: 10px
          }

          a{
            color: #959595;
            text-transform: capitalize;
            &:hover{

              text-decoration:underline ;
            }
          }

          div{
            ul{
              &:last-child{
                margin-top: 15px;
              }
            }
          }

          ul{
            margin:0 20px;
            li{
              font-size: smaller;margin: 5px 0;
            }
          }
        }
        
        .logoSide{
          position: relative;
          img{
            position: absolute;
            top: -100px
          }
          
        }
      }
    }

  

</style>