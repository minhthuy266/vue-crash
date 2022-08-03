<template>
  <h1>
    <div v-for="task in tasks" :key="task.id">
      <Task :task="task" />
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
};
</script>