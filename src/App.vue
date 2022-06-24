<template>
<div id="app">
  <TheHeader/>
</div>
</template>

<script>
import TheHeader from './components/TheHeader.vue'
export default {
  name: 'App',
  components: {TheHeader,}
}
</script>

<style lang="scss">

#app{
  height: 100vh;
  background-color: #1E2D3B;
  }
</style>
