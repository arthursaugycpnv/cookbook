src/components/RecipeCard.vue
<AppHeader />
<AppHeader />
<RecipeList />
<RecipeCard />
<template>
    <article class="recipe-card">
        <div class="recipe-image">
            {{ recipe.emoji }}
        </div>
        <div class="recipe-content">
            <h2>{{ recipe.name }}</h2>
            <p>{{ recipe.description }}</p>
            <div class="recipe-info">
                <span>⏱ {{ recipe.time }} min</span>
                <span
                    class="difficulty"
                    :class="recipe.difficulty.toLowerCase()"
                >
                    {{ recipe.difficulty }}
                </span>
            </div>
        </div>
    </article>
</template>
<script setup>
defineProps({
    recipe: {
        type: Object,
        required: true,
    },
});
</script>
<style scoped>
.recipe-card {
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 3px 12px rgba(0, 0, 0, 0.08);
    transition: transform 0.2s;
}
.recipe-card:hover {
    transform: translateY(-5px);
}
.recipe-image {
    background: #e8f1ec;
    height: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 65px;
}
.recipe-content {
    padding: 20px;
}
.recipe-content h2 {
    color: #173d35;
    margin-top: 0;
}
.recipe-content p {
    color: #666;
    font-size: 14px;
}
.recipe-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 20px;
    font-size: 13px;
}
.difficulty {
    padding: 5px 10px;
    border-radius: 20px;
    font-weight: bold;
}
.facile {
    background: #d9f5df;
    color: #23733b;
}
.moyen {
    background: #fff0ce;
    color: #946000;
}
</style>
