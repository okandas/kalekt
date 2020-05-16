<template>
  <div id="app">
  
    <TestKalekt/>
  </div>
</template>

<script>
import TestKalekt from './components/TestKalekt'
import '../node_modules/purecss/build/pure.css'
export default {
  name: 'App',
  components: {
    TestKalekt
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
</style>
