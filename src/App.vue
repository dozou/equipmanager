<template>
  <div id="app">
    <TestDB></TestDB>
    <TestButton></TestButton>
    <DebugTable></DebugTable>
  </div>
</template>

<script>
import DebugTable from "./components/DebugTable";
import TestButton from "./components/TestButton";
import TestDB from "./components/TestDB";

export default {
  name: 'App',
  components: {
    DebugTable,
    TestButton,
    TestDB
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
