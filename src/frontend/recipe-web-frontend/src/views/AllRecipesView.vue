<script setup lang="ts">
import { useRecipeStore } from '@/stores/recipeStore'
import RecipePagination from '@/components/recipe/RecipePagination.vue'
import RecipeCard from '@/components/recipe/RecipeCard.vue'

const recipeStore = useRecipeStore()
</script>

<template>
    <main class="max-w-6xl mx-auto p-6">
        <h1 class="text-2xl font-bold mb-6">Receptek</h1>
        <RecipePagination :items="recipeStore.recipes" :perPage="8" v-slot="{ items }">
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                <RecipeCard v-for="recipe in items" :key="recipe.id" :recipe="recipe" />
            </div>
        </RecipePagination>
    </main>
</template>
