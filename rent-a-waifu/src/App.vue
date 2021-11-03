<template>

  <div class="app">

  <div class="btn-container">
    <div class="updatebutton" 
    v-for="product in Products" 
    :key="product.productName">
          <button id="btn-selections"
           @click="updateProduct(product.image, product.productName, product.description, product.price)">{{product.productName}}</button> 
    </div>
  </div>

  <div class="waifu-container">
    <div class="drifting-luminescence">
      <div class="waifu-img">
        <img 
        :src="image" 
        alt="" 
        class="img-waifu">
        <div class="buttons">
          <button id="btn-waifu" v-on:click="addToCart" :click="updateTotal">Add to Cart</button>
          <div class="cart-container">
            <p class="cart">Cart({{cart}})</p>
            <p class="cartTotal">Total:${{total}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>

  </div>
    
</template>

<script>

export default {

  name:"App",

    data(){
      return{
        price: 0,
        productName:"Aether",
        description: "",
        image: require("./assets/aether.png"),
        story:["test"],
        Products:[{

          productName:"Ayaka",
              price: 300,
              description: "",
              image: require("./assets/inazuma/ayaka.png"),
              },{

          productName:"Raiden Ei",
              price: 300,
              description: "",
              image: require("./assets/inazuma/ei.png"),
              },{

          productName:"Kujou Sara",
              price: 300,
              description: "",
              image: require("./assets/inazuma/kujou.png"),
              },{

          productName:"Kokomi",
              price: 300,
              description: "",
              image: require("./assets/inazuma/kokomi.png"),

              },
              
            ],

          cart:0,
          total: 0

        }
    
  },

  methods: {
    addToCart() {
      this.cart += 1
    },
    updateProduct(image, productName, description, price ) {
      this.image = image
      this.productName = productName
      this.description = description
      this.price = price
    },
    updateTotal(){
      this.total += this.price
    }
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@500&display=swap');

* {
  padding: 0;
  margin: 0;
  font-size: 95%;
  box-sizing: border-box;
  text-decoration: none;
  list-style: none;
}

body {
  margin: 0;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  text-align: center;
  font-family: 'Noto Sans JP', sans-serif;
  background: linear-gradient(rgba(20, 4, 66, 0.4), rgba(20, 4, 66, 0.4)), url(./assets/backgrounds/cherryblossoms.jpg) no-repeat;
  background-size: cover;
}

/* app */

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  
/* container */

.waifu-container {
    background: linear-gradient(rgba(20, 4, 66, 0.4), rgba(20, 4, 66, 0.4)), url(./assets/backgrounds/christmas.jpg) no-repeat top ;
    margin: 0;
    width: 80rem;
    height: 77vh;
    max-width: 100rem;
    min-width: 50rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    border-radius: 20px;
}

/* button styles */

  .btn-container {
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
    width: 100%;
    font-weight: 300;
    font-size: 3.5rem;
    text-decoration: none;
    text-align: center;
    z-index: 2;
    margin-bottom: 1.5rem;
  }

  .buttons {
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
    width: 100%;
  }

  .buttons {
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
    width: 100%;
  }

  #btn-selections {
    width: 12rem;
    height: 5rem;
    border: none;
    font-family: "Noto Sans JP", serif;
    text-transform: uppercase;
    cursor: pointer;
    background: linear-gradient(rgba(20, 4, 66, 0.5), rgba(20, 4, 66, 0.5)), url(./assets/backgrounds/christmas.jpg) no-repeat bottom;
    color: #ffffff;
    margin-top: 1.5rem;
    padding: 0.5rem 1.5rem;
    outline: none;
    font-size: 1.5rem;
    font-weight: bold;
    text-shadow: 0 0.2rem 0.4rem rgba(0, 0, 0, 0.2);
    box-shadow: 0 0.3rem 0.5rem rgba(0, 0, 0, 0.4);
    transition: all 0.7s;
    border-radius: 15px;
    line-height: 1;
  }

  #btn-selections:hover {
    background: linear-gradient(rgba(251, 249, 255, 0.7), rgba(251, 249, 255, 0.7)), url(./assets/backgrounds/halloween.jpg) no-repeat center;
    color: rgb(11, 3, 41);
    transform: scale(1.05);
  }

  #btn-selections:active {
    transform: scale(0.75);
  }

  #btn-waifu {
    width: 17.5rem;
    height: 5rem;
    border: none;
    font-family: "Noto Sans JP", serif;
    text-transform: uppercase;
    cursor: pointer;
    background: linear-gradient(rgba(251, 249, 255, 0.7), rgba(251, 249, 255, 0.7)), url(./assets/backgrounds/halloween.jpg) no-repeat center ;
    color: rgb(11, 3, 41);
    margin-top: 1.5rem;
    padding: 0.5rem 1.5rem;
    outline: none;
    font-size: 1.75rem;
    font-weight: bold;
    text-shadow: 0 0.2rem 0.4rem rgba(0, 0, 0, 0.2);
    box-shadow: 0 0.3rem 0.5rem rgba(0, 0, 0, 0.4);
    transition: all 0.7s;
    border-radius: 15px;
    margin-left: -27.5rem;
    position: absolute;
  }

  #btn-waifu:hover {
    background: linear-gradient(rgba(20, 4, 66, 0.5), rgba(20, 4, 66, 0.5)), url(./assets/backgrounds/christmas.jpg) no-repeat bottom ;
    color: #ffffff;
    transform: scale(1.05);
  }

  #btn-waifu:active {
    transform: scale(0.75);
  }

/* images */

  .img-waifu{
    width: 45%;
    height: 100%;
    margin-top: -8rem;
    margin-bottom: 4rem;
  }

  .cart{
    font-size: 2rem;
    background-color:#A1BFD9 ;
    border-radius: 0.5rem;
    width: 10rem;
    height: 3.5rem;
    text-align: center;
    position: absolute;
    margin-left: 12rem;
    margin-top: -1rem; 
    padding: .2rem;
  }

  .cartTotal {
    font-size: 2rem;
    background-color: #A1BFD9;
    border-radius: 0.5rem;
    width: 10rem;
    height: 3.5rem;
    text-align: center;
    position: absolute;
    margin-top: -1rem;
    padding: .2rem;
}


  .updatebutton{
    width: fit-content;
    display: flex;
    flex-wrap: wrap;
  }

/* container */

.waifu-container {
    background: linear-gradient(rgba(20, 4, 66, 0.4), rgba(20, 4, 66, 0.4)), url(./assets/backgrounds/inazuma.jpg) no-repeat center ;
    margin: 0;
    width: 60rem;
    max-width: 80rem;
    min-width: 40rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    border-radius: 20px;
}


/* content */

.waifu-selections {
  display: flex;
  flex-direction: column;
}

/* img settings */

.waifu-img {
  align-self: center;
  margin-top: 4rem;
}

#kawaii-waifu {
  width: 100%;
  height: auto;
  border-radius: 20px;
}

#waifu {
  width: 75%;
  height: auto;
  border-radius: 20px;
}

</style>