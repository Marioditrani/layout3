
<script >
  
  export default {
    data(){
    return{
        obs:1,
            carouselMain:[
                {
                    
                },
                {
                    img : "../assets/img/bigimage.png",
                    paragrafo : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Error alias, molestiae iusto at magnam cumque exercitationem est culpa quae tempore maxime sed accusantium officia minima consectetur. Distinctio quaerat dolorem soluta!",
                    link : "PRENOTA TAVOLO",
                    titolo : "Titolo paragrafo1",
                },
                {
                    img : "",
                    paragrafo : "ipsum dolor sit amet consectetur adipisicing elit. Error alias, molestiae iusto at magnam cumque exercitationem est culpa quae tempore maxime sed accusantium officia minima consectetur. Distinctio quaerat dolorem soluta!",
                    link : "MENU",
                    titolo : "Titolo paragrafo2",
                },
                {
                    img : "",
                    paragrafo : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Error alias, molestiae iusto at magnam cumque exercitationem est culpa quae tempore maxime sed accusantium officia minima consectetur. Distinctio quaerat dolorem soluta!",
                    link : "PRENOTA D'ASPORTO",
                    titolo : "Titolo paragrafo3",
                }
            ]
    }
  },
  methods: {
    imgright(){
        if(this.obs == 3){
            this.obs = 1
        }else{
            this.obs ++
        } 
       
    },
    imgleft(){
        if(this.obs == 1){
            this.obs = 3
            
        }else{
            this.obs --
            
        }
            
     }
    },

  
  }
</script>


<template>

<main>
    <div class="top">
        <p class="alert">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos animi dolore ullam tenetur dolorum. Omnis, earum ipsum? Atque autem molestias velit accusamus veniam, ipsam ad magni? Nesciunt cum debitis delectus!</p>

    </div>
    <div class="bottom">
        <div class="left-home">
            <h2>titolo paragrafo</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo maiores quasi fugit. Sit maiores facilis dolorum saepe et magnam veniam! Quas reiciendis qui deserunt rerum ducimus suscipit, necessitatibus expedita ratione?</p>
            <span class="button">prenota</span>
        </div>
        <div class="right-home">
            <h2>titolo paragrafo</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo maiores quasi fugit. Sit maiores facilis dolorum saepe et magnam veniam! Quas reiciendis qui deserunt rerum ducimus suscipit, necessitatibus expedita ratione?</p>
            <span class="button">prenota</span>
        </div>
    </div>
    <div class="info">
        <div class="orari">
                  <h4>Orari d'apertura</h4>
                  <div class="cont">

                      <div class="cont-giorni">
                          <span>lunedì</span>
                          <span>martedì - domenica</span>
                      </div>
                      <div class="cont-orari">
                        <span class="time" >chiusi</span>         
                        <span class="time" >16:00 - 22:00</span>
                      </div>
                  </div>
                </div>
        <div class="dove">
            <div class="top">
                <h4>dove trovarci</h4>
            </div>
            <div class="bottom">
                <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="currentColor" class="bi bi-pin-map-fill" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M3.1 11.2a.5.5 0 0 1 .4-.2H6a.5.5 0 0 1 0 1H3.75L1.5 15h13l-2.25-3H10a.5.5 0 0 1 0-1h2.5a.5.5 0 0 1 .4.2l3 4a.5.5 0 0 1-.4.8H.5a.5.5 0 0 1-.4-.8z"/>
                <path fill-rule="evenodd" d="M4 4a4 4 0 1 1 4.5 3.969V13.5a.5.5 0 0 1-1 0V7.97A4 4 0 0 1 4 3.999z"/>
                </svg>
                <span>Via lorem ipsum 12, 34900 Citta</span>
            </div>
        </div>
    </div>
    

    
</main>
  
</template>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;


main{
    background: url('../assets/img/bigimage.png');
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 4rem;

    .alert{
        background-color: #585353;
        padding: 2rem;
        border-radius: 20px;
        width: 70%;
        margin: auto;
        margin-top: 2rem;
    }
    .bottom{
        display: flex;
        width: 90%;
        gap: 4rem;
        
        h2{
            text-transform: uppercase;
        }
        .button{
            background-color: white;
            width: 20%;
            display: flex;
            justify-content: center;
            padding: 1rem 6rem;
            align-self: center;
            margin-top: 1rem;
            color: black;
        }
        .left-home,.right-home{
            color: white;
            background-color: $c-paragrafo;
            display: flex;
            flex-direction: column;
            gap: 1rem;
            justify-content: space-between;
        }
        .left-home{
            padding: 4rem;
            height: 80%;
            width: 58%;
            h
            p{
                width: 95%;
                font-size: 20px;
            }
        }
        .right-home{
            width: 42%;
            padding: 8rem 4rem;
            p{
                width: 95%;
                font-size: 20px;
            }
        }

        
    }
    .info{
        width: 100%;
        display: flex;
        justify-content: space-between;
        h4{
            margin-bottom: 1rem;
            text-transform: uppercase;
            text-align: center;
        }
        .orari,.dove{
            background-color:#3b3737;
            padding: 1rem;
            color: white;
        }
        .cont{
            display: flex;
            justify-content: space-between;
            width: 100%;
            gap: 2rem;
        }
        .cont-giorni, .cont-orari{
            display: flex;
            flex-direction: column;
            padding-bottom: 1rem;
        }
        .cont-orari{
            text-align: end;
        }
        .dove{
            .bottom{
                width: 100%;
                display: flex;
                align-items: center;
                justify-content: space-between;
            }
        }
        
    }

}
</style>
