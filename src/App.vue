<template>
  <div>
    <h1>Список дел</h1>
    <!-- Выводим список через v-for, передавая каждый task в компонент TaskItem -->
    <TaskItem v-for="task in tasks" :key="task.id" :task="task" />
  </div>
</template>

<script>
import TaskItem from './components/TaskItem.vue';

export default {
  name: 'App',
  components: {
    TaskItem,
  },
  data() {
    return {
      tasks: [
        { id: 1, title: 'Купить продукты', text: 'Купить молоко, хлеб, овощи' },
        { id: 2, title: 'Позвонить маме', text: 'Сделать звонок маме в обед' },
        { id: 3, title: 'Завершить проект', text: 'Дописать документацию и протестировать' },
      ],
    };
  },
};
</script>

<style>
/* Для стилей*/
</style>