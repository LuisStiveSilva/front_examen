<template>
  <div id="app">
    <Home />
    <p class="credits">
      Databot 2022.
    </p>
  </div>
</template>

<script>
import Home from './views/Home.vue';

export default {
  name: 'App',
  components: {
    Home,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
body {
  margin: 0; 
}
.container {
  max-width: 1300px;
  width: 100%;
  margin: auto;
}
.credits {
  font-size: 12px;
  color: #b2b2b2;
  text-align: center;
  margin: 2rem;
}
</style>
