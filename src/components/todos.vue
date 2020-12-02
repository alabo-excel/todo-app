<template>
  <div class="text-center">
    <h3>Todos</h3>
    <div class="row justify-content-center">
      <div
        class="col-3 todo m-3 text-white p-4"
        v-for="todo in allTodos"
        :key="todo.id"
      >
        <div @click="deleteTodo(todo.id)" class="float-right">
          <img :src="require('../assets/Icon_Exit.png')" alt="" />
        </div><br>
        {{ todo.title }}
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters, mapActions } from "vuex";

export default {
  name: "Todos",
  methods: {
    ...mapActions(["fetchTodos", "deleteTodo"]),
  },
  computed: mapGetters(["allTodos"]),
  created() {
    this.fetchTodos();
  },
};
</script>
<style>
.todo {
  background-color: rgb(173, 160, 135);
  border-radius: 10px;
}
</style>
