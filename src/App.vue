<template>
  <div id="app">
    <img src="./assets/logo.png">
    <!-- <HelloWorld/> -->
    <Events/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Events from './components/Event'
export default {
  name: 'App',
  components: { /*绑定组件 */
    HelloWorld,
    Events
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
