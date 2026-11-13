<script setup>
import RecipeCard from "./RecipeCard.vue";
defineProps({
    recipes: {
        type: Array,
        required: true,
    },
});
</script>
<template>
    <section class="recipes">
        <div class="section-title">
            <h2>Mes recettes</h2>
            <p>{{ recipes.length }} recettes disponibles</p>
        </div>
        <div class="recipe-grid">
            <RecipeCard
                v-for="recipe in recipes"
                :key="recipe.id"
                :recipe="recipe"
            />
        </div>
    </section>
</template>
<style scoped>
.recipes {
    padding: 30px 40px;
}
.section-title {
    margin-bottom: 25px;
}
.section-title h2 {
    color: #173d35;
    margin-bottom: 5px;
}
.section-title p {
    color: #777;
    font-size: 14px;
}
.recipe-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 75px;
}
@media (max-width: 750px) {
    .recipe-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}
@media (max-width: 500px) {
    .recipe-grid {
        grid-template-columns: 1fr;
    }
    .recipes {
        padding: 20px;
    }
}
</style>
