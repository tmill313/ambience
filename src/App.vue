<template>
  <div id="app">
    <Ambience msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Ambience from './components/Ambience.vue'

export default {
  name: 'app',
  components: {
    Ambience
  }
}
</script>

<style>
body {
    background-color: #21D19F;
    font-family: 'Raleway', sans-serif;
     color: white;

}
</style>
