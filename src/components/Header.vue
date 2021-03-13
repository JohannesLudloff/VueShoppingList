<template>
  <header>
    <h1>{{ title }}</h1>
    <Button text="Hinzufügen" color="black" @btn-click="$emit('toggle-add-task')" />
  </header>
</template>

<script>
import Button from "./Button";
export default {
  name: "Header",
  components: { Button },
  props: {
    title: String,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
