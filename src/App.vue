<template>
  <div id="app">
    <HelloWorld />
    <ExampleWord />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ExampleWord from './components/examples.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ExampleWord
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
