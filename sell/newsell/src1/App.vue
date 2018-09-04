<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
  html,body{
    font-size: 24px;
    min-height: 700px;
    min-width: 900px;
  }
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size: 24px;
  /*margin-top: 60px;*/
}
*{
  padding: 0;
  margin: 0;
}
  @media (max-width:600px) {

  }
</style>
