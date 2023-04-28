

<script>

export default {
  name: "_Card",
  props:{
    item : Object
  }
}
</script>

<template>

  <div class="card">
    <div class="containerImg">
      <img :src="item.thumb" alt="">
    </div>
    
    <div class="name">
      <h5>{{ item.series }}</h5>
    </div>
  </div>
   
</template>

<style lang="scss" scoped>
      .card{
        height: 220px;
        margin-bottom: 20px;
        padding: 10px;


        .containerImg{
          height: 180px;
          overflow: hidden;
          margin-bottom: 10px;
        }

        img{
          object-fit: contain;
          width: 100%;
          
        }

        h5{
          color: white;
          text-transform: uppercase;
        }
      }
</style>