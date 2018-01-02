<template>
  <div id="app">
    <h1> Reading the CSV file data</h1>

 <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
 
import {Line} from 'vue-chartjs'
export default {
   extends: Line,
   name: 'app'
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
  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
