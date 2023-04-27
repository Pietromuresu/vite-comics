
<script>
import {headerMenus, DCMenu, shopMenu, sitesMenu, mediaLinks} from '../js/all-menus'
export default {
  name: 'Footer',
  data(){
    return{
      headerMenus,
      DCMenu,
      shopMenu,
      sitesMenu,
      mediaLinks
    }
  },
  methods:{
    getImage(img){
      return new URL(`../assets/img/${img}`, import.meta.url).href
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
    <div class="container">
      
      <div>

        <div class="signUpBtn">
          <h4>SIGN-UP NOW!</h4>
        </div>

      </div>

      <div class="mediaLinks">

        <h3>FOLLOW US</h3>
        <ul>
          <li v-for="(link, index) in mediaLinks" :key="index">
            <a :href="link.href">
              <img :src="getImage(link.icon)" alt="ICON">
            </a>
          </li>
        </ul>

      </div>

    </div>

    
  </div>
</template>

<style lang="scss" scoped>
@import '../scss/partials/general';
@import '../scss/partials/variables';

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

    .footerBottom{
      @include flexMe(vertical);
        height: 100px;
        background:$lighter-black;
      .container{
        @include flexMe(vertical);
        justify-content: space-between;



        .signUpBtn{
          color: white;
          border: 1px solid $blue;
          padding: 10px;

          h4{
            font-weight: 800;
          }
        }
        
        .mediaLinks{
          height: 100%;
          @include flexMe(vertical);
          

          h3{
            font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            font-weight: bolder;
            color: $blue;
            margin-right: 20px;
          }

          ul{
            display: flex;

            li{
              margin: 0 10px;
            }
          }
        }
      }
      
    }

  

</style>