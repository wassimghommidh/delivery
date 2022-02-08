<template>
 
  <div id="app">
<AdminMenu />
  </div>
</template>

<script>
import AdminMenu from "../src/AdminMenu.vue"
export default {
  name: "App",
  components: {
    AdminMenu,
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
