
<script>
import Header from './components/_Header.vue';
import Main from './components/_Main.vue';
import servicesBand from './components/_ServicesBand.vue';
export default {
  name: 'App',

  components:{
    Header,
    Main,
    servicesBand
  },
data(){
  return{
    
  }
}
}
</script>

<template>
<Header />
<Main/>
<servicesBand/>
</template>

<style lang="scss" >
@use './scss/main.scss'


</style>