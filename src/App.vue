<template>
  <div id="app">
    <input type="text" v-model="text">
    <div>{{upperText}}</div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      text: "Hello"
    };
  },
  computed: {
    upperText() {
      setTimeout(() => {
        this.text.toUpperCase();
      }, 1000);
      return this.text;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
