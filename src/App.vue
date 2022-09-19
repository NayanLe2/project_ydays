
<template>
    <header_bloc></header_bloc>
    <nav_bar></nav_bar>
</template>

<script>
import header_bloc from './components/header_bloc.vue'
import nav_bar from './components/nav_bar.vue'


export default {
  name: 'App',
  components: {
      header_bloc,
      nav_bar
  }
}
</script>

<style></style>
