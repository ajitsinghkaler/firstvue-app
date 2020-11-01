<template>
  <nuxt-link :to="'/recipes/' + id">
    <article class="recipe">
      <div
        class="thumbnail"
        :style="{ backgroundImage: 'url(' + thumbnail + ')' }"
      ></div>
      <h1>{{ title }}</h1>
      <p>{{ previewText }}</p>
    </article>
  </nuxt-link>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  props: ["thumbnail", "title", "previewText", "id"],
});
</script>

<style scoped>
.recipe {
  box-sizing: border-box;
  width: 200px;
  padding: 8px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #aaa;
  margin: 10px;
}

a {
  text-decoration: none;
  color: black;
}

.thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
</style>
