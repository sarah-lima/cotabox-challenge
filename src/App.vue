<template>
  <div>
    <Menu />
    <DataChart />
  </div>
</template>

<script>
import DataChart from "./components/DataChart.vue";
import Menu from './components/menu/Menu.vue'

export default {
  name: "App",
  components: {
    DataChart,
    Menu
  },
};
</script>

<style>
#app, body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin: 0;
  padding: 0;
}
</style>
