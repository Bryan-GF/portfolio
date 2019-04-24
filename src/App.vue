<template>
  <div id="app">
    <div>
      <Nav/>
    </div>
    <div class='contentWrapper'>
      <Intro/>
      <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App"/>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Nav from './components/Nav.vue'
import Intro from './components/Intro.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Nav,
    Intro
  } 
}
</script>

<style>

@import url('https://fonts.googleapis.com/css?family=Pacifico');

body {
  margin: 0;
}

#app {
  font-family: sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.contentWrapper {
  padding: 110px 0 0 0;
}

</style>
