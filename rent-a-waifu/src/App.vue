<template>

  <div class="app">

  <div class="btn-container">
    <div class="updatebutton" v-for="product in Products" :key="product.productName">
          <button id="btn-selections" @click="updateProduct(product.image, product.productName, product.description)">{{product.productName}}</button> 
    </div>
  </div>

    <div class="product">

      <div class="product-info">
        <h2 class="product-name">{{productName + " " +description}}</h2>
      </div>

      <img :src="image" alt="" class="image">

      <div class="story">Storyline
        <h1 v-for="story in story" :key="story">{{story}}</h1>
      </div>

      <div class="buttons">
        <button id="btn-waifu" v-on:click="addToCart">Add to Cart</button>

      <div class="cart-container">
        <p class="cart">Cart({{cart}})</p>
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
        productName:"Aether",
        description: "",
        image: require("./assets/aether.png"),
        story:["test"],
        Products:[{

          productName:"Ayaka",
              description: "",
              image: require("./assets/inazuma/ayaka.png"),
              story:["no"],
              },{

          productName:"Raiden Ei",
              description: "",
              image: require("./assets/inazuma/ei.png"),
              },{

          productName:"Kujou Sara",
              description: "",
              image: require("./assets/inazuma/kujou.png"),
              },{

          productName:"Kokomi",
              description: "",
              image: require("./assets/inazuma/kokomi.png"),

              },
            ],

          cart:0

        }
    
  },

  methods: {
    addToCart() {
      this.cart += 1
    },
    updateProduct(image,productName,description ) {
      this.image = image
      this.productName = productName
      this.description = description
    },
  }
}

</script>

<style>

  html,
  body {
    font-family: "Source Sans Pro", sans-serif;
    box-sizing: border-box;
    padding: 0;
    margin: 0;
    font-size: 92.5%;
    color: black;
    height: 100vh;
    font-weight: 500;
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
  
  .product{
    margin: 4rem;
    margin-top: 0;
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
    width: 25rem;
    height: 5rem;
    border: none;
    font-family: "Noto Sans JP", serif;
    text-transform: uppercase;
    cursor: pointer;
    background: linear-gradient(rgba(20, 4, 66, 0.5), rgba(20, 4, 66, 0.5));
    color: #ffffff;
    margin-top: 1.5rem;
    padding: 0.5rem 1.5rem;
    outline: none;
    font-size: 2rem;
    font-weight: bold;
    text-shadow: 0 0.2rem 0.4rem rgba(0, 0, 0, 0.2);
    box-shadow: 0 0.3rem 0.5rem rgba(0, 0, 0, 0.4);
    transition: all 0.7s;
    border-radius: 15px;
  }

  #btn-selections:hover {
    background: linear-gradient(rgba(251, 249, 255, 0.7), rgba(251, 249, 255, 0.7));
    color: rgb(11, 3, 41);
    transform: scale(1.05);
  }

  #btn-selections:active {
    transform: scale(0.75);
  }

  #btn-waifu {
    width: 25rem;
    height: 5rem;
    border: none;
    font-family: "Noto Sans JP", serif;
    text-transform: uppercase;
    cursor: pointer;
    background: linear-gradient(rgba(20, 4, 66, 0.5), rgba(20, 4, 66, 0.5));
    color: #ffffff;
    margin-top: 1.5rem;
    padding: 0.5rem 1.5rem;
    outline: none;
    font-size: 2rem;
    font-weight: bold;
    text-shadow: 0 0.2rem 0.4rem rgba(0, 0, 0, 0.2);
    box-shadow: 0 0.3rem 0.5rem rgba(0, 0, 0, 0.4);
    transition: all 0.7s;
    border-radius: 15px;
  }

  #btn-waifu:hover {
    background: linear-gradient(rgba(251, 249, 255, 0.7), rgba(251, 249, 255, 0.7));
    color: rgb(11, 3, 41);
    transform: scale(1.05);
  }

  #btn-waifu:active {
    transform: scale(0.75);
  }

/* images */


  .image{
    width: 25%;
    height: 100%;

  }

  .cart{
    font-size: 2rem;
    background-color:#A1BFD9 ;
    border-radius: 0.5rem;
    width: 10rem;
    height: 3.5rem;
    text-align: center;
    padding-top: 1rem;
  }

  .updatebutton{
    width: fit-content;
    display: flex;
    flex-wrap: wrap;
  }

</style>