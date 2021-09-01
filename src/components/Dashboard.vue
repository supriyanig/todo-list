<template>
  <div class="container">
    <CompletedItems></CompletedItems>
    <AddTodo></AddTodo>
    <Todos></Todos>
  </div>
</template>

<script>
import AddTodo from './AddTodo.vue'
import Todos from './Todos.vue'
import CompletedItems from './CompletedItems.vue'
export default {
  components: {
    AddTodo,
    Todos,
    CompletedItems
  }
 
}
</script>

<style>
body {
  font-family: Helvetica, sans-serif;
}
</style>