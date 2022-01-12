<template>
  <div id="app">
    <pre>{{ data }}</pre>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "App",
  data() {
    return {
      data: "Loading",
    };
  },
  mounted() {
    axios
      .get("https://penta.conversa-dev.it/api/v1/akern?asmm=abc&token=abc")
      .then((response) => {})
      .catch((error) => {
        this.data = error.response.data;
      });
  },
};
</script>

<style>
</style>
