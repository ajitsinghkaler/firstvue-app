<template>
  <header>
    <nav>
      <ul>
        <li>
          <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/recipes">Recipes</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>


<style scoped>
header {
  height: 30px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
li {
  margin: 0 10px;
}
</style>
