<template>
  <div class="app-container">
    <h1 class="main-title">📋 Мой список дел</h1>
    
    <!-- Утренние задачи -->
    <section>
      <h2 class="section-title">🌅 Утро</h2>
      <div class="task-list">
        <TaskItem v-for="task in morningTasks" :key="task.id" :task="task" />
      </div>
    </section>
    
    <!-- Вечерние задачи -->
    <section>
      <h2 class="section-title">🌇 Вечер</h2>
      <div class="task-list">
        <TaskItem v-for="task in eveningTasks" :key="task.id" :task="task" />
      </div>
    </section>
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
      // Задачи на утро с подпунктами
      morningTasks: [
        {
          id: 1,
          title: 'Тренировки',
          text: 'Пресс качать',
          subtasks: ['Делать Бегит', 'Висеть Турник', 'Выполнять Анжуманя'],
        },
        {
          id: 2,
          title: 'Кушац',
          text: 'Живот урчит бульк-бульк',
          subtasks: ['3 порции риса с пловом из чайханы', 'Выпить БЦАшку со вкусом мультифрукта'],
        },
        {
          id: 3,
          title: 'Учебный процесс',
          text: 'Поставить свечку против отчисления',
          subtasks: ['Поплакать перед выполнением задач', 'Посмотреть рилсы про отчисление'],
        },
      ],
      // Задачи на вечер с подпунктами
      eveningTasks: [
        {
          id: 4,
          title: 'Тренировки',
          text: 'Пресс качать',
          subtasks: ['Делать Бегит', 'Висеть Турник', 'Выполнять Анжуманя'],
        },
        {
          id: 5,
          title: 'Кушац',
          text: '2 шаурмы XXL в сытом хищнике',
          subtasks: ['Выпить литр L-карнитина', 'Съесть 4 литровых пакета креатинчика'],
        },
        {
          id: 6,
          title: 'Подготовка к учёбе на завтра',
          text: 'Крикнуть в окно: "Халява, приди"',
          subtasks: ['Порассуждать о смысле жизни', 'Посмотреть новости про договорнячок'],
        },
      ],
    };
  },
};
</script>

<style>
.app-container {
  max-width: 800px;
  margin: 40px auto;
  padding: 20px;
  font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
  background-color: #8bd1ff;
  border-radius: 12px;
  box-shadow: 0 4px 16px rgba(255, 0, 0, 0.07);
}

.main-title {
  text-align: center;
  font-size: 2.5em;
  color: #474888;
  margin-bottom: 30px;
}

/* Заголовки разделов */
.section-title {
  font-size: 2em;
  margin-top: 30px;
  margin-bottom: 15px;
  text-align: center;
  color: #474888;
}

.task-list {
  display: flex;
  flex-direction: column;
  gap: 15px;
}
</style>