<script setup>
  import {ref} from "vue";

  defineEmits(['add'])

  const task = ref("")
</script>

<template>
  <div>
    <input type="text" v-model="task"/>
    <button @click="$emit('add', task)">Add Task</button>
  </div>
</template>

<style scoped>

</style>