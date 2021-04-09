<template>
  <div>
    <section v-if="arreglo && arreglo.length == 0">
      <p>Aquí irán las edades</p>
    </section>
    <section v-else>
      <ul>
        <li v-for="(el,index) in arreglo" :key="index">Edad N°{{index + 1}}: {{el.edad}}</li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    arreglo: {
      type: Array,
      default: () => []
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
