
<script >

export default {
    
  data(){
    return{
      sideMenuValue: 0,
      infomenu: 0,
        
    }
  },
  methods: {
    openside() {
        if (this.sideMenuValue) {
            this.sideMenuValue = 0
        } else {
            this.sideMenuValue = 1

        }
        console.log(this.sideMenuValue)
    
    },
    infoside() {
        if (this.infomenu) {
            this.infomenu = 0
        } else {
            this.infomenu = 1
        }
    },
    
  },

  
  }
  
</script>


<template>
  <header>
    <div class="left-header">
      <div class="logo">
      </div>
      <div class="title">
        <span>nome locale </span>
      </div>
    </div>
    <div class="right-header">
      <div class="nav">
         <router-link :to="{ name: 'home' }" class="link" >home</router-link>
         <router-link :to="{ name: 'prenotaServizio' }" class="link"  >prenota tavolo</router-link>
         <router-link :to="{ name: 'prenota' }" class="link"  >prenota asporto</router-link>
         <router-link :to="{ name: 'chi-siamo' }" class="link"  >chi siamo</router-link>
         <router-link :to="{ name: 'Contatti' }" class="link"  >contatti</router-link>
         <router-link :to="{ name: 'menu' }" class="link"  >menu</router-link>
      </div>
    </div>
    
    <div class="nav-mb">
      <div class="btn-menu" @click="openside" >
        <div class="l2" :class="sideMenuValue? 'l1-on':''"></div>
        <div class="l2" :class="sideMenuValue? 'l2-on':''"></div>
        <div class="l2" :class="sideMenuValue? 'l3-on':''"></div>
      </div>
    </div>

    <div  :class="this.sideMenuValue? 'nav-mb-on': 'nav-mb-off'">
        <div :class="this.sideMenuValue? 'top-on': 'top-off'">
         <router-link :to="{ name: 'home' }" class="link" :class="infomenu ?   'menu-off': '' " @click="openside">home</router-link>
         <router-link :to="{ name: 'prenotaServizio' }" class="link" :class="infomenu ?   'menu-off': '' " @click="openside" >prenota tavolo</router-link>
         <router-link :to="{ name: 'prenota' }" class="link" :class="infomenu ?   'menu-off': '' " @click="openside" >prenota asporto</router-link>
         <router-link :to="{ name: 'chi-siamo' }" class="link" :class="infomenu ?   'menu-off': '' " @click="openside" >chi siamo</router-link>
         <router-link :to="{ name: 'Contatti' }" class="link" :class="infomenu ?   'menu-off': '' " @click="openside" >contatti</router-link>
         <router-link :to="{ name: 'menu' }" class="link" :class="infomenu ?   'menu-off': '' " @click="openside" >menu</router-link>
         <div class="nav-link info"  :class="infomenu ? 'info-on' : 'info-off'">
              <div :class="infomenu ? 'top-info-on' : 'top-info-off'" >
                <h4 @click="infoside">info</h4>
                <span  @click="infoside" :class="infomenu ? 'info-btn' : 'info-n'">+</span>
              </div>

              <div :class="infomenu ? 'main-info-on' : 'main-info-off'">

                <div class="sec-1">
                  <h4>Dove puoi trovarci</h4>
                  <p>Monsano</p>
                </div>

                <div class="sec-2">
                  <h4>Orari d'apertura</h4>
                  <div class="cont-giorni">
                      <span>lunedì</span>
                      <span>martedì</span>
                      <span>giovedì</span>
                      <span>venerdì</span>
                      <span>sabato</span>
                      <span>domenica</span>
                  </div>
                  <div class="cont-orari">
                    <span class="time" >chiusi</span>         
                    <span class="time" >16:00 - 22:00</span>
                    <span class="time" >16:00 - 22:00</span>
                    <span class="time" >16:00 - 22:00</span>
                    <span class="time" >16:00 - 22:00</span>
                    <span class="time" >16:00 - 22:00</span>
                  </div>
                </div>

              </div>

              <div :class="infomenu ? 'sec-3' : 'sec-3-off'" >
                Kojo sushi, PI: 1231231231231, privacy policy, product by FUTURE+
              </div>
           </div>
        </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;
.nav-link.info{
  color: white;
  font-size: 22px;
  .top-info-on{
    padding: 10px;
    width:100%;
    @include dfc;
    justify-content: space-between;
  }
  .top-info-off{
    @include dfc;
    
  }


  .info-on{
  height:100%;
  background-color: $c-header;
  width:100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: all .2s linear;
  }
  
  .info-btn{
  transform: rotateZ(765deg);
  font-size:40px;
  padding:20px;
  transition: all .2s linear;
  }
  .info-n{
    position: relative;
    z-index: 300;
  }
  
  .main-info-on{
  @include dfc;
  flex-direction: column;
  justify-content: space-between;
  text-align:center;
  gap: 25px;
  .sec-1{
  
      @include dfj;
      flex-direction: column;
      gap: 10px;
      width: 100%;
  
  
      h4{
        font-size:20px;
  
      }
      p{
        font-size:16px;
      }
    }
  .sec-2{
    @include dfj;
    flex-wrap: wrap;
    gap: .6rem;
    width: 100%;
    justify-content: space-around;
    padding-bottom: 1rem;
    h4{
      
      width: 100%;
      padding-bottom:20px;
      font-size: 20px;
    }
    .cont-giorni, .cont-orari{
      font-size: 15px;
      @include dfj;
      flex-direction: column;
      gap: .3rem;
      text-align: left;
      text-transform: uppercase;
      
      .time{
        text-align: center;
      }
    }
  
  }
  
  }
  .main-info-off{
  display: none;
  }
  
  .sec-3{
  background-color: rgba(0, 0, 0, 0.43);
  font-size: 10px;
  padding: 10px;
  }
  .sec-3-off{
  display: none;
  }
}

.menu-off{
display:none;
}
.info-on{
  background-color: $c-header;
  width:100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: all .2s linear;
  }

header{

  background-color: rgba(0, 0, 0, 0.445);
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 6rem;
  text-transform: uppercase;
  z-index: 5!important;
  height: 200px;
  .left-header{
    display: flex;
    align-items: center;
    gap: 20%;
    width: 20%;
    .logo{
      width: 200px;
      aspect-ratio: 1;
      background-color: $c-nav;
    }
    .title{
      font-size: 30px;
    }

  }
  .right-header{
    width: 70%;
        .nav{
      background-color: $c-nav;
      display: flex;
     justify-content: space-between;
      padding: 3rem;

      .link{
        color: white;
        text-transform: uppercase;
        font-size: 22px;
      }
    }
  }
  
}


.nav-mb{
    display: none;
    position: relative;
    width: 100%;   
  .btn-menu{
    position: fixed;
    right: 50px;
    top: 70px;
    flex-direction: column;
    gap: .7rem;
    align-items: flex-end;
    display: flex;
    z-index: 5!important;
    .l2{
      z-index: 10;
      width: 50px;
      height: 5px;
      border-radius: 20px;
      background-color: white;
     
    }
    
    
    }
    
    
  }

  .nav-mb-on{
    position: fixed;
    top: 0;
    left: 0;
    background-color: #270000;
    width: 100%;
    height: 100%;
    transition: all .3s linear;
   
  
    }

    .nav-mb-off{
    position: fixed;
    top: 0;
    left: 0;
    background-color: #270000;
    width: 100%;
    height: 0;
    transition: all .2s linear;

    

  }

  .l1-on{
    transform: rotateZ(-45deg);
  }
  .l2-on{
    position: fixed;
    transform: rotateZ(45deg);
  }
  .l3-on{
    display: none;
  }
  
  .top-off{
    
display: none;
opacity: 0;
transition: display .3s linear;
transition: opacity 1s linear 2s;



    
  }
  .top-on{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    padding: 10%;
    height: 100%;
    margin-top: 4rem;
    
    .link{
      color: white;
      font-size: 23px;
      z-index: 10!important;
      position: relative!important;
    }
  }

  

@media (max-width: 1700px) {
  
  .right-header{
    display: none!important;
  }
  .nav-mb{
    display: block!important;
    z-index: 2!important;
  }
  
 
}
@media (max-width: 700px) {
  
  header{
    padding: 5rem 2rem!important;
  }

}
@media (max-width: 600px) {
  
  header{
    .left-header{
      .logo{
        width: 150px;
      }
      .title{
        display: none;
      }
    }
  }

}
</style>
