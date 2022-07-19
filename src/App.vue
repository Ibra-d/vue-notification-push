<template>
  <div class="home">
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
body {
  margin: 0;
}
</style>
