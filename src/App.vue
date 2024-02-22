<script >
  
  import AppHeader from './components/AppHeader.vue'
 
  
  
  

  export default {
  components:{  AppHeader,  }
  }
</script>

<template>

  <div class="container">
    
      <AppHeader class="header"/>
      <router-view class="page"></router-view>
    
  </div>
 

  
</template>

<style lang="scss">
@use './assets/styles/general.scss' as *;

.container{
  width: 100vw;
  height: 100vh;
 
  .header{
    height: 10%;
  }
  .page{
    height: 90%;
  }
 
}

@media (max-width: 1600px) {
  .nav{
    display: none !important;
  }
  .page{
    width: 100%!important;
  }
  
}


</style>
