<template>
  <div id="app">
    <HelloWorld msg="This is a simple Vue.js app that calculates the cube of a number"/>
  </div>
</template>

<script>
import HelloWorld from '../components/HelloWorld.vue';
export default {
  name: 'About',
  components: {
    HelloWorld
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
