
<script >

  
  export default {
    
    components:{},
    data(){
    return{
        
    }
  },
  methods: {
   
    },

  
  }
</script>


<template>
    <main>
        <div class="header">
            <div class="left-header">
                <div class="logo"></div>
                <h1 class="title">Nome Locale</h1>
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
        </div>
        <div class="center-home">
            <div class="top-center">
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aspernatur, quo eos? Accusantium, neque temporibus. Magni aliquid aspernatur temporibus nemo, ipsam, quidem numquam cupiditate quo labore ut eligendi sequi libero voluptatum.</p>
            </div>
            <div class="bottom-center">
                <div class="left-center">
                    <h2>titolo paragrafo</h2>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Earum animi omnis debitis provident, cupiditate iure porro enim eum similique quia eos maiores blanditiis accusamus, sit commodi quaerat iste optio unde!</p>
                    <span class="button">prenota</span>
                </div>
                <div class="right-center">
                    <h2>titolo paragrafo</h2>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Earum animi omnis debitis provident, cupiditate iure porro enim eum similique quia eos maiores blanditiis accusamus, sit commodi quaerat iste optio unde!</p>
                    <span class="button">prenota</span>
                </div>
            </div>
        </div>
        <div class="bottom-home">
            <div class="left-bottom"></div>
            <div class="right-bottom"></div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;


main::before{
  content:' ';
  position: fixed;
  inset: 0;
  z-index: -1000;
  height: 100%;
  width: 100vw;
  background: url('../assets/img/bigimage.png');
  background-repeat: no-repeat;
  background-size: cover;
}


main{
    display: flex;
    flex-direction: column;
    gap: 2rem;
    .header{
        background-color: rgba(0, 0, 0, 0.575);
        padding: 1.5rem;
        margin-top: 1rem;
        display: flex;
        justify-content: space-between;
        width: 100%;
        .left-header{
                display: flex;
                align-items: center;
                width: 30%;
                justify-content: space-around;
            .logo{
                width: 150px;
                aspect-ratio: 1;
                background-color: $c-nav;
            }
            .title{
               font-size: 50px;
               text-transform: uppercase;
               text-align: center;
               color: white;
            }
        }
        .right-header{
            width: 70%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 4rem;

            .nav{
                background-color: $c-nav;
                width: 100%;
                display: flex;
                justify-content: space-between;
                padding: 2rem;
            }
            .link{
                color: white;
                text-transform: uppercase;
                font-size: 25px;
                
            }
        }

    }
    .center-home{
        .top-center{
            display: flex;
            justify-content: center;
            padding: 1rem;
            p{
                width: 70%;
                background-color: $c-nav;
                padding: 2rem;
                color: white;
                font-size: 15px;
                border-radius: 20px;
            }
        }
        .bottom-center{
            width: 95%;
            margin: 0 auto;
            display: flex;
            gap: 4rem;
            padding-top: 4rem;
            color: white;
            
            .left-center{
                background-color: #585858c0;
                width: 60%;
                display: flex;
                flex-direction: column;
                padding: 3rem;
                gap: 1rem;
                height: 60%;
                .button{
                    background-color: white;
                    color: black;
                    width: 20%;
                    padding: .5rem 1rem;
                    align-self: center;
                    text-align: center;
                    text-transform: uppercase;
                    margin-top: 1rem;
                }
            }
            .right-center{
                background-color: #585858c0;
                width: 40%;
                display: flex;
                flex-direction: column;
                padding: 6rem;
                gap: 1rem;
                .button{
                    background-color: white;
                    color: black;
                    width: 20%;
                    padding: .5rem 1rem;
                    align-self: center;
                    text-align: center;
                    text-transform: uppercase;
                    margin-top: 1rem;
                }
            }
        }
    }
    .bottom-home{
        width: 100%;
        

    }
}
</style>
