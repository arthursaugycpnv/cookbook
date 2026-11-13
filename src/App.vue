<script setup>
import AppHeader from "./components/AppHeader.vue";
import RecipeList from "./components/RecipeList.vue";
import RecipeFooter from "./components/RecipeFooter.vue";

// Les données de nos recettes
const recipes = [
    {
        id: 1,
        name: "Spaghetti",
        description: "Délicieuses pâtes à la sauce tomate.",
        time: 20,
        difficulty: "Facile",
        emoji: "🍝",
        persons: 3,
    },
    {
        id: 2,
        name: "Pizza",
        description: "Pizza maison aux légumes.",
        time: 35,
        difficulty: "Moyen",
        emoji: "🍕",
        persons: 2,
    },
    {
        id: 3,
        name: "Gâteau",
        description: "Gâteau au chocolat fait maison.",
        time: 45,
        difficulty: "Facile",
        emoji: "🍰",
        persons: 2,
    },
    {
        id: 4,
        name: "Salade",
        description: "Salade fraîche de saison",
        time: 15,
        difficulty: "Difficile",
        emoji: "🥗",
        persons: 2,
    },
];
</script>

<template>
    <div class="app">
        <!-- Composant enfant : en-tête -->
        <AppHeader />
        <main>
            <section class="hero">
                <h1>Bienvenue dans ma cuisine !</h1>
                <p>Découvrez des recettes simples et délicieuses.</p>
            </section>
            <!-- Composant enfant : liste des recettes -->
            <RecipeList :recipes="recipes" />
        </main>
        <RecipeFooter />
    </div>
</template>

<style scoped>
.app {
    min-height: 100vh;
}
.hero {
    background: #e8f1ec;
    padding: 50px 30px;
    text-align: center;
}
.hero h1 {
    color: #173d35;
    font-size: 32px;
}
.hero p {
    color: #526b60;
}
</style>
