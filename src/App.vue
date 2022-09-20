
<template>
    <header_bloc></header_bloc>
    <nav_bar></nav_bar>
    <bottom_project></bottom_project>
    <bottom_besoins></bottom_besoins>
    <bottom_contact></bottom_contact>
</template>

<script>
import header_bloc from './components/header_bloc.vue'
import nav_bar from './components/nav_bar.vue'
import bottom_project from './components/bottom_project.vue'
import bottom_besoins from './components/bottom_besoins.vue'
import bottom_contact from './components/bottom_contact.vue'


export default {
  name: 'App',
  components: {
      header_bloc,
      nav_bar,
      bottom_project,
      bottom_besoins,
      bottom_contact
  }
}
</script>

<style></style>
