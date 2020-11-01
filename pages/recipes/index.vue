{<template>
  <section class="recipes">
    <Recipe
    v-for="recipe in recipes"
    :key="recipe.id"
      id="1"
      :thumbnail="recipe.thumbnail"
      :title="recipe.title"
      :previewText="recipe.previewText"
    />
  </section>
</template>

<script lang="ts">
import Vue from "vue";
import Recipe from "@/components/Recipe.vue";
export default Vue.extend({
  components: {
    Recipe,
  },
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: "1",
              title: "Delicious Pizza",
              previewText: "Awesome Pizza",
              thumbnail:
                "https://images.immediate.co.uk/production/volatile/sites/30/2020/08/chorizo-mozarella-gnocchi-bake-cropped-9ab73a3.jpg?webp=true&quality=90&resize=620%2C563",
            },
          ],
        });
      }, 1500);
    });
  },
});
</script>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
</style>

