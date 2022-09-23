<template>
<div class="bottom_project">
    <h1 class="bottom_title">Proposer plus qu’une simple friperie</h1>
    <div class="article" v-for="art in articles" :key="art.id">
        <h4>➡️ {{ art.titre }}</h4>
        <p>{{ art.article }}</p>
    </div>
</div>
</template>

<script>
export default {
    name: "bottom_project",
    data() {
        return {
            articles: [
                {
                    titre: "Achat de vêtements au détail 👕",
                    article: "Proposer des vêtements vintage de " +
                        "marques et de qualité, est notre priorité. " +
                        "Nous souhaiterions proposer une large " +
                        "gamme de vêtements de toutes catégories."
                },
                {
                    titre: "Vêtements d’occasions remis à neuf ♻️",
                    article: "Pour un prix plus abordable, certains " +
                        "vêtements d’occasion remis à neuf seront " +
                        "proposés. "
                },
                {
                    titre: "Boites Mystère 📦",
                    article: "Pour un prix plus abordable, certains " +
                        "vêtements d’occasion remis à neuf seront " +
                        "proposés. "
                }
            ]
        }
    }
}
</script>

<style scoped>

</style>