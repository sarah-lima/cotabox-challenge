<template>
    <header>
      <Input placeholder="First name" />
      <Input placeholder="Last name" />
      <Input placeholder="Participation" />
      <Button text="SEND" />
    </header>
</template>

<script>
import Button from '../button/Button.vue';
import Input from "../input/Input.vue";

export default {
  name: "Menu",
  components: {
    Input,
    Button,
  },
};
</script>

<style scoped>
header {
  background-color: #00b8e2;
  width: 100%;
  height: 75px;
  display: flex;
  align-items: center;
  gap: 10px;
  justify-content: center;
}
</style>
