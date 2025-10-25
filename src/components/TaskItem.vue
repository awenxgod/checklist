<template>
  <div class="task-card">
    <h3>{{ task.title }}</h3>
    <p>{{ task.text }}</p>
  </div>
</template>

<script>
export default {
  name: 'TaskItem',
  props: {
    task: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.task-card {
  border: 1px solid #ccc;
  padding: 10px;
  margin-bottom: 10px;
  border-radius: 4px;
  background-color: #f9f9f9;
  color: #000000; /* Чёрный цвет текста */
}
</style>
