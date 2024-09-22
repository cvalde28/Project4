<template>
    <div>
      <h2>Recipes</h2>
      <ul>
        <li v-for="recipe in recipes" @click="selectRecipe(recipe)" :key="recipe.id">
          {{ recipe.name }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: ['recipes'],
    methods: {
      selectRecipe(recipe) {
        this.$emit('recipe-selected', recipe);
      },
    },
  };
  </script>
  