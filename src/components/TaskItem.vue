<template>
  <div class="task-card">
    <h3 class="task-title">🎯 {{ task.title }}</h3>
    <p class="task-text">📝 {{ task.text }}</p>
    <!-- Вложенные подпункты -->
    <ul v-if="task.subtasks && task.subtasks.length" class="subtasks">
      <li v-for="(subtask, index) in task.subtasks" :key="index">🔹 {{ subtask }}</li>
    </ul>
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
  border: 1px solid #399fff;
  padding: 15px;
  margin-bottom: 15px;
  border-radius: 8px;
  background-color: #e3e3ff;
  box-shadow: 0 4px 8px rgba(255, 51, 51, 0.1);
  transition: box-shadow 0.2s ease, transform 0.2s ease;
}

.task-card:hover {
  box-shadow: 0 8px 16px rgba(38, 0, 255, 0.2);
  transform: translateY(-2px);
}

.task-title {
  margin: 0 0 10px;
  font-size: 1.2em;
  color: #455b72;
}

.task-text {
  margin: 0;
  font-size: 1em;
  color: #34495e;
}

/* Стиль для подпунктов */
.subtasks {
  margin-top: 10px;
  padding-left: 20px;
  list-style-type: none;
}

.subtasks li {
  margin-bottom: 5px;
}
</style>