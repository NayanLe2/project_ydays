<template>
    <div class="bottom_besoins">
        <h1 class="bottom_title">Les postes à pourvoir</h1>
        <div class="article" v-for="art in articles" :key="art.id">
            <h4>➡️ {{ art.titre }}</h4>
            <p>{{ art.article }}</p>
        </div>

    </div>
</template>

<script>
export default {
    name: "bottom_besoins",
    data() {
        return {
            articles: [
                {
                    titre: "Informatique 💻",
                    article: "Conception / finitions du site web en " +
                        "ligne de la friperie :\n" +
                        "Backend/Frontend"
                },
                {
                    titre: "Marketing & Communication 📈",
                    article: "Lancer la commercialisation\n" +
                        "\t- Gestion des stocks / budgets\n" +
                        "Communication sur le projet :\n" +
                        "\t- Compte TikTok\n" +
                        "\t- Compte Instagram : " +
                        "@shopnextclothes"
                },
                {
                    titre: "Créa Design 🎨",
                    article: "Refonte des designs, du site web en \n" +
                        "ligne de la friperie."
                },
                {
                    titre: "Audiovisuel 📷",
                    article: "Mise en valeur des vêtements par la\n" +
                        "photographie:\n" +
                        "\t- Photos portées, travailler\n" +
                        "l'aperçu du produit afin de booster les\n" +
                        "ventes"
                }
            ]
        }
    }
}
</script>

<style scoped>

</style>