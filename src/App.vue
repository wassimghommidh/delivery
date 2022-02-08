<template>
 
  <div id="app">
<AdminMenu />
  <!-- <Cardrestaurant/> -->
  </div>
</template>
 
<script>
import AdminMenu from "./components/AdminMenu.vue"

// import {Cardrestaurant} from "./components/Cardrestaurant"

export default {
  name: "App",
  components: {
    AdminMenu,
    // Cardrestaurant
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
