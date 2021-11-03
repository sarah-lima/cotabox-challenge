<template>
  <button @click="click">{{ text }}</button>
</template>
<script>
export default {
  props: {
    click: Function,
    text: String,
  },
};
</script>

<style scoped>
button {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 2px solid #ffffff;
  background-color: transparent;
  color: #ffffff;
  width: 100px;
  height: 35px;
  padding: 0 10px;
  font-weight: 800;
  border-radius: 2px;
}
</style>