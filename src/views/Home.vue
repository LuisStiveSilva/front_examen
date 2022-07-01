<template>
  <section class="home">
    <div class="header"></div>
    <p class="rocket">🚀</p>
    <h1>Test Front-End Databot</h1>
    <h3 class="text-center">Víncula la API de la NASA 👇</h3>
    <div class="container">
      <div class="info_box">
        <p class="text-center">Oculta este contenedor y reemplaza con tus tarjetas aquí.</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {

}
</script>

<style scoped>
.header {
  background-color: #2981EF;
  height: 75px;
}
.rocket {
  font-size: 55px;
  margin: 5rem auto .5rem
}
h1 {
  font-size: 55px;
  margin: 1rem auto .5rem;
}
.info_box {
  border: 1px dashed #cdcdcd;
  border-radius: 1rem;
  margin: 5rem auto;
  padding: 2rem;
  display: flex;
  width: 1000px;
  height: 250px;
}
.text-center {
  text-align: center;
  margin: auto;
}
</style>
