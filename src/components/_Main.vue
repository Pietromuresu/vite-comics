<script>
import Card from './partials/_Card.vue';
import products from '../../dc-comics.json';

export default {
  name: 'Main',
  components:{
    Card
  },
  data(){
    return{
      products
    }
  }

}
</script>

<template>
  <div>
    <div class="jumbotron"></div>

    <div class="products">
      <div class="container">
        <h3 class="currentSeriesTitle">
          CURRENT SERIES
        </h3>

        <div class="card-wrapper">
          <div class="cardContainer" v-for="(product, index) in products" :key="index">
            <Card :item ="product" />
          </div>
        </div>
      </div>
      <div class="loadBtn">
        <h4>LOAD MORE</h4>
      </div>
    </div>

    
  </div>
</template>

<style lang="scss" scoped>
  @import '../scss/partials/variables';
  @import '../scss/partials/general';

  div{
    .jumbotron{
      background-image: url(../assets/img/jumbotron.jpg);
      background-size: cover;
      height: 350px;
      padding: 20px;
      @include flexMe(vertical)
    }


    .products{

      background: $black;
      width: 100%;


      .currentSeriesTitle{
        position: absolute;
        display: block;
        line-height: 30px;
        background: $blue;
        color: white;
        padding: 5px 20px;
       top: calc(-40px / 2);
      }
    }   

    .card-wrapper{
      display: flex;
      flex-wrap: wrap;
      flex-basis: calc(100% / 6);
      padding-top: 40px;

      .cardContainer{
        width: calc(100% / 6);

      }


    }

    .loadBtn{
      @include flexMe(horizontal);

      h4{
        line-height: 30px;
        padding: 5px 20px;
        background-color: $blue;
        margin-bottom: 20px;
        color: white;
      }
    }
  }  

  .container{
    width: 80%;
    margin: 0 auto; 
    position: relative;
  }
</style>