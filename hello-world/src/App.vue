<template>

    <div id="app">
      <div class="cart">
        <p>Cart({{ cart.length }})</p>
      </div>
      <product :premium="premium" @add-to-cart="updateCart"></product>
  </div> 


</template>

<script src="https://cdn.jsdelivr.net/npm/vue@2.5.13/dist/vue.js">

// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
}

</script>

<style>

@import "./css/main.css";

</style>
