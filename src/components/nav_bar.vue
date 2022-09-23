<template>
    <div class="nav_bar">
        <svg @click="beforePage" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="arrow-small-left">
            <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 12h-15m0 0l6.75 6.75M4.5 12l6.75-6.75" />
        </svg>
        <p id="page-title">Le Projet</p>
        <svg @click="nextPage" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="arrow-small-right">
            <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 12h15m0 0l-6.75-6.75M19.5 12l-6.75 6.75" />
        </svg>
    </div>
</template>

<script>
export default {
    name: "nav_bar",
    /*
    props: {
        title: String
    },
    data() {
        return {
            page_title: this.title
        }
    },
     */
    methods: {
        nextPage: function () {
            let pageTitle = document.getElementById("page-title");
            if (pageTitle.innerHTML === "Le Projet") {
                pageTitle.innerHTML = "Nos Besoins";
                // change to page 'Nous Contacter'
            } else if (pageTitle.innerHTML === "Nos Besoins") {
                pageTitle.innerHTML = "Nous Contacter";
                // change to page 'Le Projet'
            } else if (pageTitle.innerHTML === "Nous Contacter") {
                pageTitle.innerHTML = "Le Projet";
                // change to page 'Nos Besoins'
            }
            /*
            let pageTitle = document.getElementById("page-title");
            if ( this.page_title.value === "Le Projet") {
                this.page_title.value = "Nos Besoins";
            }else if ( this.page_title.value === "Nos Besoins") {
                this.page_title.value = "Nous Contacter";
            } else if ( this.page_title.value === "Nous Contacter") {
                this.page_title.value = "Le Projet";
            }
            */
        },
        beforePage: function () {
            let pageTitle = document.getElementById("page-title");
            if (pageTitle.innerHTML === 'Le Projet') {
                pageTitle.innerHTML = 'Nous Contacter';
                // change to page 'Nous Contacter'
            } else if (pageTitle.innerHTML === 'Nos Besoins') {
                pageTitle.innerHTML = 'Le Projet';
                // change to page 'Le Projet'
            } else if (pageTitle.innerHTML === 'Nous Contacter') {
                pageTitle.innerHTML = 'Nos Besoins';
                // change to page 'Nos Besoins'
            }
            /*
            if ( this.page_title === 'Le Projet') {
                this.page_title = 'Nos Besoins';
            }else if ( this.title === 'Nos Besoins') {
                this.page_title = 'Nous Contacter';
            } else if ( this.title === 'Nous Contacter') {
                this.page_title = 'Le Projet';
            }
            */
        }
    }
}
</script>

<style scoped>

</style>