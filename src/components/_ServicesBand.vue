<script>
import {services} from '../js/all-menus'
export default {
  name: 'ServicesBand',
  data(){
    return{
      services
    }
  },
  methods:{
    getImage(image){
      return new URL('../assets/img/image', import.meta.url).href
    }
  }
}
</script>

<template>
  <div class="servicesBand">
    <ul>
      <li v-for="(service, index) in services" :key="index">
        <img :src="getImage(service.img)" alt="img">
        <a :href="service.href"> {{ service.text }}</a>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
@import '../scss/partials/variables';
  .servicesBand{
    @include flexMe(both);
    height: 150px;
    background-color: $blue;
    ul{
      display: flex;
      li{
        color: white;
        display: flex;
        margin: 0 20px;
        text-transform: uppercase;
        font-size: small;
        img{
          height: 20px;
        }
        a{
          color: white;
          &:hover{
            text-decoration: underline;
          }
        }
      }
    }
  }
</style>