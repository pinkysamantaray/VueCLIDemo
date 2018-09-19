<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="shadow">
    
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.shadow {
  height: 20vh;
  width: 50vw;
  margin: 0 auto;
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
