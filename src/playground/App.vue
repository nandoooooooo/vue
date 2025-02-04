<script setup>
  import TaskAdder from "./components/TaskAdder.vue"
  import {ref} from "vue";

  const tasks = ref([
      "Rasen mähen",
      "Spanisch lernen",
  ])
</script>

<template>
  <TaskAdder @add="tasks.push($event)"></TaskAdder>
  <dl>
    <dd v-for="task in tasks" :key="task">
      {{ task }}
    </dd>
  </dl>
</template>

<style scoped>

</style>
