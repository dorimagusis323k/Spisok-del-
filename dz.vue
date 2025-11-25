<template>
  <div id="app">
    <h1>Мои задачи</h1>
    <div class="tasks-container">
      <TaskItem 
        v-for="task in tasks" 
        :key="task.id" 
        :task="task"
      />
    </div>
  </div>
</template>

<script>
import TaskItem from './components/TaskItem.vue'

export default {
  name: 'App',
  components: {
    TaskItem
  },
  data() {
    return {
      tasks: [
        {
          id: 1,
          title: 'Изучить Vue.js',
          text: 'Освоить основы фреймворка Vue.js, включая компоненты, директивы и состояние'
        },
        {
          id: 2,
          title: 'Создать проект',
          text: 'Разработать приложение для управления задачами с использованием Vue'
        },
        {
          id: 3,
          title: 'Деплой на GitHub',
          text: 'Выложить готовый проект на GitHub Pages'
        },
        {
          id: 4,
          title: 'Оптимизация',
          text: 'Добавить дополнительные функции: фильтрацию, поиск и редактирование задач'
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

h1 {
  text-align: center;
  color: #2c3e50;
  margin-bottom: 30px;
}

.tasks-container {
  display: grid;
  gap: 20px;
}
</style>