<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <FileTable></FileTable>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import FileTable from "./components/FileTable";

export default {
  name: 'App',
  components: {
    HelloWorld,
    FileTable
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
