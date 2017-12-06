<template>
  <div id="app">
    <nav-bar disable-ripple="last" title="张三"></nav-bar>
    <div class="container-fluid">
    </div>
    <router-view/>
  </div>
</template>
<script>
import navBar from './components/nav'
export default {
  name:'app',
  components:{ navBar }
}
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
