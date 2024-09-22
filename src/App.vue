<template>
  <div>
    <RecipeList :recipes="recipes" @recipe-selected="handleRecipeSelect" />
    <RecipeDetail :recipe="selectedRecipe" />
    <Calculator :selectedRecipe="selectedRecipe" />
  </div>
</template>

<script>
import RecipeList from './components/RecipeList.vue';
import RecipeDetail from './components/RecipeDetail.vue';
import Calculator from './components/Calculator.vue';

export default {
  components: {
    RecipeList,
    RecipeDetail,
    Calculator,
  },
  data() {
    return {
      recipes: [
        { id: 1, name: 'Spaghetti', cost: 10, calories: 500 },
        { id: 2, name: 'Salad', cost: 5, calories: 200 },
      ],
      selectedRecipe: null,
    };
  },
  methods: {
    handleRecipeSelect(recipe) {
      this.selectedRecipe = recipe;
    },
  },
};
</script>
