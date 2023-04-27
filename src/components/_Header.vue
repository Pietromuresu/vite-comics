<script>
import { headerMenus }  from "../js/all-menus";
export default {
  name: 'Header',

  data(){ 
     
    return{
      headerMenus
    }
  }
}
</script>

<template>
  
  <header>
    <div class="container">

      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
      </div>


      <div class="headerMenu">
        <div class="hamMenu">
          <h1 class="displayNone"><i class="fa-solid fa-bars"></i></h1>
        </div>
        <nav>
          <ul>
           <li
              v-for="(link, index) in headerMenus"
              :key="index"
              :class="{'active' : link.isActive}">

              <a href="#">{{link.text}}</a>
           
            </li>
          </ul>
        </nav>
      </div>

    </div>
  </header>

</template>

<style lang="scss" scoped>
@import '../scss/partials/variables';
  header{
    margin-top: 1rem ;
    .container{

      display: flex;
      justify-content: space-between;
      align-items: center;
   
      img{
        height: 80px;
      }

      // .hamMenu{
      //   display: none;
      // }

      ul{
        display: flex;
        li{
          margin: 0 10px;

          &:hover,
          &.active{
            border-bottom: 5px solid $blue;

            a{
              color: $blue;
            }
          }

          a{
            line-height: 80px;
            color: $font-black;
            text-transform: uppercase;
            font-size: smaller;
          }
        }
     }
    }

    @media screen and (max-width: 900px) {
      .hamMenu{
        h1{

          display: block;
        }
      }  
      nav{
       display: none;
      }
    }


  }

</style>