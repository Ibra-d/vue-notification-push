<template>
  <div class="home">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Notif />
  </div>
</template>

<script>
import Notif from "./components/Notif.vue";

export default {
  name: "App",
  components: {
    Notif,
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
  margin-top: 60px;
}
</style>
