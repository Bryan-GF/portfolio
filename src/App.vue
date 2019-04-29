<template>
  <div id="app">
    <div>
      <Nav/>
    </div>
    <div class='contentWrapper'>
      <Intro/>
      <Projects/>
      <Contact/>
    </div>
  </div>
</template>

<script>
import Nav from './components/Nav.vue';
import Intro from './components/Intro.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';

export default {
  name: 'app',
  components: {
    Nav,
    Intro,
    Projects,
    Contact
  } 
}
</script>

<style>

@import url('https://fonts.googleapis.com/css?family=Pacifico');

body {
  margin: 0;
  color: #212121;
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
