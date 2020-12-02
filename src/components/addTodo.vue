<template>
  <div class="text-center">
    <h3>Add todo</h3>
    <div>
      <form @submit="onSubmit">
        <input id="form" type="text" v-model="title" placeholder="Add Todo" />
        <input id="submit" type="submit" value="Submit" />
      </form>
    </div>
  </div>
</template>

<script>
import { mapActions } from 'vuex';

export default {
    data(){
        return{
            title: ''
        }
    },
    methods: {
        ...mapActions(['addTodo']),
    onSubmit(e){
        e.preventDefault();
        this.addTodo(this.title)
    }
    },
};

</script>
<style>
#form {
  width: 75%;
}
input {
  padding: 10px;
  border-radius: 10px;
  border: none;
  margin: 10px;
}
#submit {
        background-color: rgb(173, 160, 135);
  color: white;
}
</style>
