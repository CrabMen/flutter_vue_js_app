<template>
  <div id="app">
    <h1>Hello Vue.js!</h1>
    <button @click="sendMessage">Send Message to Flutter</button>
  </div>
</template>

<script>
export default {
  methods: {
    sendMessage() {
      if (window.Toaster) {
        window.Toaster.postMessage("Hello from Vue.js");
      } else {
        console.error("sendMessageToFlutter is not defined");
      }
    },
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
