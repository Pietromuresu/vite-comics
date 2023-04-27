
<script>
import Header from './components/_Header.vue';
import Main from './components/_Main.vue';
import servicesBand from './components/_ServicesBand.vue';
import Footer from './components/_Footer.vue'
export default {
  name: 'App',

  components:{
    Header,
    Main,
    servicesBand,
    Footer
  },
data(){
  return{
    
  }
}
}
</script>

<template>
<Header />
<Main />
<servicesBand />
<Footer />
</template>

<style lang="scss" >
@use './scss/main.scss'


</style>