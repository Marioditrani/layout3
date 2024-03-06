<script >
  
  
  
  
  

  export default {
 
  }
</script>

<template>

  <div class="container">
    
    
      <router-view class="page"></router-view>
    
  </div>
 

  
</template>

<style lang="scss">
@use './assets/styles/general.scss' as *;

.container{
  width: 100vw;
  height: 100vh;
  font-family: "Roboto", sans-serif;
  
  .page{
    width: 100vw;

  }
 
}

@media (max-width: 1600px) {
  
  .page{
    width: 100%!important;
  }
  
}


</style>
