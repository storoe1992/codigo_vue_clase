<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld :arreglo="miarreglo"/>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'
export default {
  
  name: 'App',
  data() {
    return {
      miarreglo: [{edad:31},{edad:36},{edad:30}]
    }
  },
  components: {
    HelloWorld,
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
