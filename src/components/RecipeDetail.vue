<template>
    <div v-if="recipe">
      <h3>{{ recipe.name }}</h3>
      <p>Cost: {{ recipe.cost }}</p>
      <p>Calories: {{ recipe.calories }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: ['recipe'],
  };
  </script>
  