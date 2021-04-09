<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <input v-model="edad" type="text">
    <button @click="ingresarEdad()">Agregar Edad</button>
    <HelloWorld :arreglo="miarreglo"/>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'
export default {
  
  name: 'App',
  data() {
    return {
      miarreglo: [{edad:31},{edad:36},{edad:30}],
      edad: "",
    }
  },
  components: {
    HelloWorld,
  },
  methods: {
    ingresarEdad() {
      if(this.edad == "") return
      this.miarreglo.push({edad: this.edad})
      this.edad = ""
    }
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
