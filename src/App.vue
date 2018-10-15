<template>
  <div id="app" class="shadow">
    <img src="./assets/logo.png" class="brandImage">
    <HelloWorld msg="Welcome to CSS!!"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
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
}
.brandImage {
  width: 50pt;
}
.shadow {
  padding: 10px;
  margin: 10px auto;
  height: 94vh;
  background: #ffffff;
  position: relative;
}
.shadow:before {
  content: '';
  position:absolute;
  top: -2px;
  left: -2px;
  background: linear-gradient(45deg, #0000ff, #00ff00, #ff0000, #ffff00);
  background-size: 400%;
  width: calc(100% + 4px);
  height: calc(100% + 4px);
  z-index: -1;
  animation: animate 20s linear infinite;
}

@keyframes animate {
  0% {
    background-position: 0 0;
  }
  50% {
    background-position: 400% 0;
  }
  100% {
    background-position: 0 0;
  }
}
</style>
