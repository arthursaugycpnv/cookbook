<template>
    <header class="header">
        <div class="logo">🍲 CookBook</div>
        <nav>
            <a href="#">Accueil</a>
            <a href="#">Mes recettes</a>
        </nav>
    </header>
</template>
<script setup></script>
<style scoped>
.header {
    background-color: #173d35;
    color: white;
    padding: 20px 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.logo {
    font-size: 24px;
    font-weight: bold;
}
nav {
    display: flex;
    gap: 25px;
}
nav a {
    color: white;
    text-decoration: none;
}
nav a:hover {
    color: #b8dfc5;
}
</style>
