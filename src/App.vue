<template>
  <div>
    <Menu />
    <Container />
  </div>
</template>

<script>
import Container from './components/container/Container.vue';
import Menu from './components/menu/Menu.vue'

export default {
  name: "App",
  components: {
    Menu,
    Container
  },
};
</script>

<style>
#app, body {
  font-family: 'Roboto', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin: 0;
  padding: 0;
}
</style>
