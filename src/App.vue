
<template>
  <header_bloc></header_bloc>
</template>

<script>
import header_bloc from './components/header_bloc.vue'

export default {
  name: 'App',
  components: {
      header_bloc
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
