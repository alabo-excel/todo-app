<template>
  <div id="app">
  <addTodo />
  <filterTodo />
  <todos />
  </div>
</template>

<script>
import todos from './components/todos.vue'
import addTodo from './components/addTodo.vue'
import filterTodo from './components/filterTodo.vue'

export default {
  name: 'App',
  components: {
    todos,
    addTodo,
    filterTodo
  }
}
</script>

<style>
    body{
        overflow-x: hiden!important;
        background-color: wheat;
    }
</style>
