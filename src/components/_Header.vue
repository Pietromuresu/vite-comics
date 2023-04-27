<script>
export default {
  name: 'Header',
  data(){
    return{

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
        <nav>
          <ul>
            <li class="active"><a href="#">Characters</a></li>
            <li><a href="#">comics</a></li>
            <li><a href="#">movies</a></li>
            <li><a href="#">tv</a></li>
            <li><a href="#">games</a></li>
            <li><a href="#">collectibles</a></li>
            <li><a href="#">videos</a></li>
            <li><a href="#">fans</a></li>
            <li><a href="#">news</a></li>
            <li><a href="#">shop</a></li>
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
   
      img{
        height: 80px;
      }
      ul{
        display: flex;
        li{
          margin: 0 10px;

          &:hover,
          &.active{
            border-bottom: 5px solid $blue;
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
  }

</style>