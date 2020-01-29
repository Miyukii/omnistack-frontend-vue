<template>
  <div id="app">
    <Side />
    <Main />
  </div>
</template>

<script>
import Side from './components/Side.vue'
import Main from './components/Main.vue'

export default {
  name: 'app',
  components: {
    Side,
    Main
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
@import url('https://fonts.googleapis.com/css?family=Roboto:400,700&display=swap');

* {
    margin: 0;
    outline: 0;
    box-sizing: 0;
}

html, body, #root {
    height: 100%;
}

body {
    background: #e5e6f0;
    -webkit-font-smoothing: antialiased;
}

body, input, button {
    font-family: Roboto, sans-serif;
}
</style>
