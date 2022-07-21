<template>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700;900&display=swap" rel="stylesheet">
  <headerComponent class="header-component"/>
  <router-view />
  <footerComponent />
</template>

<script>
import headerComponent from "./components/headerComponent.vue";
import footerComponent from "./components/footerComponent.vue";

export default {
  name: 'App',
  components: {
    headerComponent,
    footerComponent,
  },
  async mounted() {
    let elements = await fetch("https://raw.githubusercontent.com/danila-derenchenko/forApi/main/cart.json")
    let result = await elements.json()
    this.$store.dispatch("firstLoadingCart", result)
  }
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    font-family: 'Lato', sans-serif;
  }
  .container {
    width: 1140px;
    margin: 0 auto;
  }
  .forHeader {
    padding-top: 75px;
  }
  .header-component {
    position: fixed;
  }
</style>