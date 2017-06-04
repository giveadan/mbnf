<template>
  <div id="app">
    <hero></hero>
    <hello></hello>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Hero from './components/Hero'

export default {
  name: 'app',
  components: {
    Hero,
    Hello
  }
}
</script>

<style>
#app {
  font-family: 'Helvetica', Helvetica, Arial, sans-serif;
  color: #2c3e50;
}
body {
  margin:0;
  position: relative;
}
</style>
