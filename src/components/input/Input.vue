<template>
  <input :placeholder="placeholder" :value="value" />
</template>

<script>
export default {
  props: {
    placeholder: String,
    value: String,
  },
};
</script>

<style scoped>
input {
  border: none;
  width: 200px;
  height: 35px;
  border-radius: 2px;
  padding: 0 10px;
}
</style>