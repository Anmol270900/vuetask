<template>
  <div id="app">
    <HelloWorld msg="Enter a number to obtain its cube : "/>
    <Number v-on:calCube="calCube" />
    <HelloWorld v-bind:cube="`this.cube`" />
    <h1>{{this.cube}}</h1>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Number from './components/Number';

export default {
  name: 'App',
  components: {
    HelloWorld,
    Number
  },
  data() {
    return {
      cube: 0
    }
  },
  methods: {
    calCube(number) {
      this.cube = number*number*number;
    }
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
