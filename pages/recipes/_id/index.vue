<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img :src="recipe.thumbnail" :alt="recipe.title" />
    </div>
    <p>{{ recipe.descriptionText }}</p>
  </section>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1",
              title: "Delicious Pizza",
              previewText: "Awesome Pizza",
              descriptionText: "This is delicious",
              thumbnail:
                "https://images.immediate.co.uk/production/volatile/sites/30/2020/08/chorizo-mozarella-gnocchi-bake-cropped-9ab73a3.jpg?webp=true&quality=90&resize=620%2C563",
            },
          ].find((el) => el.id === context.params.id),
        });
      }, 1500);
    });
  },
});
</script>

<style scoped>
.single-recipe {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
  flex-flow: column;
}
</style>
