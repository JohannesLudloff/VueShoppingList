<template>
  <div @dblclick="$emit('toggle-reminder', task.id)" :class="[task.reminder ? 'reminder' : '', 'task']">
    <h3>{{ task.text }}<i class="fas fa-times" @click="ClickDelete(task.id)"></i></h3>
    <p>{{ task.day }}</p>
  </div>
</template>

<script>
export default {
  name: "Task",
  props: {
    task: Object,
  },
  methods: {
    ClickDelete(id) {
      this.$emit("delete-task", id);
    },
  },
};
</script>

<style>
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px;
  cursor: pointer;
}
.task.reminder {
  border-left: 3px solid green;
}
.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
