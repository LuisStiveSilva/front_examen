<template>
  <section class="home">
    <div class="header" />
    <p class="rocket">
      🚀
    </p>
    <h1>Test Front-End Databot</h1>
    <h3 class="text-center">
      Víncula la API de la NASA 👇
    </h3>
    <div class="container">
      <div 
        v-show="false" 
        class="info_box"
      >
        <p class="text-center">
          Oculta este contenedor y reemplaza con tus tarjetas aquí.
        </p>
      </div>
      <div class="card_container">
        <div 
          v-for="item in data" 
          :key="item.id"
          class="card"
        >
          <img 
            :src="item.img_src" 
            alt="" 
            class="card_image"
          >
          <p class="card_camera">
            {{ item.camera.full_name }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from "axios";
export default {
  name: "Home",
  data() {
    return {
      data: null,
    };
  },
  mounted() {
    this.getData();
  },
  methods: {
    getData() {
      axios
        .get(
          `https://api.nasa.gov/mars-photos/api/v1/rovers/curiosity/photos?sol=1000&api_key=`
        )
        .then((res) => (this.data = res.data.photos.splice(0, 3)))
        .catch((error) => console.error(error));
    },
  },
};
</script>

<style scoped>
.header {
  background-color: #2981ef;
  height: 75px;
}
.rocket {
  font-size: 55px;
  margin: 5rem auto 0.5rem;
}
h1 {
  font-size: 55px;
  margin: 1rem auto 0.5rem;
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
.card_container{
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  margin: 10px auto;
}
.card{
  background: rgba(0,0,0,0.6);
  border-radius: 10px;
  overflow: hidden;
  width: 250px;
}
.card_image{
  width: 100%;
  height: auto;
}
.card_camera{
  color:#eee
}
</style>
