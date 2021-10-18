<template>
  <router-view/>
</template>

<script>

</script>

<style lang="less">
html {
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: inherit;
}
body {
  margin: 0px;
  padding: 0px;
}
@font-face {
  font-family: "swatchit";
  src: local("swatchit"),
  url(../src/assets/fonts/swatchit.TTF) format("truetype");
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.red-bg {
  background-color: #D52028;
}
</style>
