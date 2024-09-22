<template>
    <div>
      <h4>Total Cost: {{ totalCost }}</h4>
      <h4>Total Calories: {{ totalCalories }}</h4>
    </div>
  </template>
  
  <script>
  export default {
    props: ['selectedRecipe'],
    computed: {
      totalCost() {
        return this.selectedRecipe ? this.selectedRecipe.cost : 0;
      },
      totalCalories() {
        return this.selectedRecipe ? this.selectedRecipe.calories : 0;
      },
    },
  };
  </script>
  