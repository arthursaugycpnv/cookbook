# Exercice 5

Expliquer avec vos propres mots.

## 1. Quel est le composant parent ?

App.vue est le composant racine : c'est le parent de tous les autres composants de l'application.

## 2. Quels sont les composants enfants ?

- Dans App.vue, on retrouve 3 enfants : AppHeader, RecipeList et RecipeFooter.
- Dans RecipeList, on trouve un enfant : RecipeCard.

## 3. Quel composant contient les données ?

App.vue. Les recettes y sont déclarées dans la partie script setup, sous forme d'un tableau d'objets nommé recipes.

## 4. Comment les données arrivent-elles dans RecipeCard ?

Elles descendent de parent en enfant grâce aux props, en deux étapes :

1. App.vue → RecipeList : App.vue passe tout le tableau à RecipeList avec l'attribut :recipes="recipes". RecipeList le reçoit en déclarant la prop recipes avec defineProps.
2. RecipeList → RecipeCard : RecipeList parcourt le tableau avec v-for="recipe in recipes" et crée une RecipeCard par recette. Il lui transmet une seule recette avec l'attribut :recipe="recipe". RecipeCard la reçoit en déclarant la prop recipe.
