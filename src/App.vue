<template>
  <div id="app">
    <hero></hero>
  </div>
</template>

<script>
import Hero from './components/Hero'

export default {
  name: 'app',
  components: {
    Hero
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
