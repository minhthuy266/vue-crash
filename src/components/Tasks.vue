<template>
  <h1>
    <div v-for="task in tasks" :key="task.id">
      <Task
        @toggle-reminder="$emit('toggle-reminder', task.id)"
        @delete-task="$emit('delete-task', task.id)"
        :task="task"
      />
    </div>
  </h1>
</template>

<script>
import Task from "./Task";

export default {
  name: "TasksComponent",
  props: {
    tasks: Array,
  },
  components: {
    Task,
  },
  emits: ["delete-task", "toggle-reminder"],
};
</script>
