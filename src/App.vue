
<template>
    <header_bloc></header_bloc>
    <div class="nav_bar">
        <svg @click="beforePage" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="arrow-small-left">
            <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 12h-15m0 0l6.75 6.75M4.5 12l6.75-6.75" />
        </svg>
        <p id="page-title">Le Projet</p>
        <svg @click="nextPage" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="arrow-small-right">
            <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 12h15m0 0l-6.75-6.75M19.5 12l-6.75 6.75" />
        </svg>
    </div>
    <bottom_project id="bottom_project" style="display: flex"></bottom_project>
    <bottom_besoins id="bottom_besoins" style="display: none"></bottom_besoins>
    <bottom_contact id="bottom_contact" style="display: none"></bottom_contact>
</template>

<script>
import header_bloc from './components/header_bloc.vue'
import bottom_project from './components/bottom_project.vue'
import bottom_besoins from './components/bottom_besoins.vue'
import bottom_contact from './components/bottom_contact.vue'


export default {
    name: 'App',
    components: {
      header_bloc,
      bottom_project,
      bottom_besoins,
      bottom_contact
  },
    methods: {
        nextPage: function () {
            let pageTitle = document.getElementById("page-title");
            let bottom_project = document.getElementById("bottom_project");
            let bottom_besoins = document.getElementById("bottom_besoins");
            let bottom_contact = document.getElementById("bottom_contact");
            if (pageTitle.innerHTML === "Le Projet") {
                pageTitle.innerHTML = "Nos Besoins";
                bottom_project.style.display = "none";
                bottom_besoins.style.display = "flex";
                bottom_contact.style.display = "none";
            } else if (pageTitle.innerHTML === "Nos Besoins") {
                pageTitle.innerHTML = "Nous Contacter";
                bottom_project.style.display = "none";
                bottom_besoins.style.display = "none";
                bottom_contact.style.display = "flex";
            } else if (pageTitle.innerHTML === "Nous Contacter") {
                pageTitle.innerHTML = "Le Projet";
                bottom_project.style.display = "flex";
                bottom_besoins.style.display = "none";
                bottom_contact.style.display = "none";
            }
        },
        beforePage: function () {
            let pageTitle = document.getElementById("page-title");
            let bottom_project = document.getElementById("bottom_project");
            let bottom_besoins = document.getElementById("bottom_besoins");
            let bottom_contact = document.getElementById("bottom_contact");
            if (pageTitle.innerHTML === 'Le Projet') {
                pageTitle.innerHTML = 'Nous Contacter';
                bottom_project.style.display = "none";
                bottom_besoins.style.display = "none";
                bottom_contact.style.display = "flex";
            } else if (pageTitle.innerHTML === 'Nos Besoins') {
                pageTitle.innerHTML = 'Le Projet';
                bottom_project.style.display = "flex";
                bottom_besoins.style.display = "none";
                bottom_contact.style.display = "none";
            } else if (pageTitle.innerHTML === 'Nous Contacter') {
                pageTitle.innerHTML = 'Nos Besoins';
                bottom_project.style.display = "none";
                bottom_besoins.style.display = "flex";
                bottom_contact.style.display = "none";
            }
        }
    }
}
</script>

<style>
</style>
