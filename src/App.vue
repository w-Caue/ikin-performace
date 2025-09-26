<template>
  <TheHeader />
  <ProductCarrosel />
  <FirstPoster />
  <TheFooter />
</template>

<script>
import TheHeader from "./components/TheHeader";
import ProductCarrosel from "./components/ProductCarrosel";
import FirstPoster from "./components/FirstPoster";
import TheFooter from "./components/TheFooter.vue";

export default {
  name: "App",
  components: {
    TheHeader,
    ProductCarrosel,
    FirstPoster,
    TheFooter,
  },
  data() {
    return {
      
    }
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
