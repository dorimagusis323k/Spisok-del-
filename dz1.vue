<template>
  <div class="task-card">
    <h3 class="task-title">{{ task.title }}</h3>
    <p class="task-text">{{ task.text }}</p>
    <div class="task-id">ID: {{ task.id }}</div>
  </div>
</template>

<script>
export default {
  name: 'TaskItem',
  props: {
    task: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.task-card {
  background: #ffffff;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.task-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
}

.task-title {
  color: #2c3e50;
  margin: 0 0 10px 0;
  font-size: 1.2em;
  font-weight: 600;
}

.task-text {
  color: #555;
  line-height: 1.5;
  margin: 0 0 15px 0;
}

.task-id {
  color: #888;
  font-size: 0.8em;
  text-align: right;
}
</style>