<script setup>
import AppHeader from "./components/AppHeader.vue";
</script>

<template>
    <div>
        <AppHeader />
        <main>
            <h1>Bienvenue dans ma cuisine !</h1>
            <p>Découvrez des recettes simples et délicieuses.</p>
        </main>
    </div>
</template>
<style scoped>
main {
    padding: 40px;
    text-align: center;
}
h1 {
    color: #173d35;
}
</style>
