/* eslint-disable */

<template>
  <HelloWorld msg="Welcome to Your Vue.js App"/>;
  <MyHomePage />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import MyHomePage from './components/MyHomePage.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    MyHomePage
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
