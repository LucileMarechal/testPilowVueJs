<template>
  <div id="app">
    <h1 class="title">Combien d'oreillers dans votre vie ?</h1>
    <pillow />
  </div>
</template>
<script>
import Pillow from "./components/Pillow.vue"



export default {
  name: 'App',
  components: {

    Pillow,
  }
}

</script>

<style>
#app {
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  text-align: center;
  width: 100%;
  height: 100%;
  margin: 100px auto 0;
}

.title {
  color: #5ad8c9;
}
</style>

