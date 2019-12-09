<template>
  <div id="app" class="container">
    <h1 class="text-center">todo App</h1>
    <form @submit.prevent="addTodo()">
      <div class="form-group">
        <label for="newTodo">New Todo</label>
        <input
          v-model="newTodo"
          type="text"
          class="form-control"
          id="newTodo"
          aria-describedby="newTodoHelp"
          placeholder="walk the dog..."
        />
        <small id="newTodoHelp" class="form-text text-muted">Enter a new Todo</small>
      </div>
      <button type="submit" class="btn btn-primary">Add todo</button>
    </form>
    <ul class="list-group">
      <li  v-for="todo in todos" class="list-group-item">{{ todo }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      newTodo: "",
      todos: []
    };
  },
  methods: {
    addTodo() {
      this.todos.push(this.newTodo);
    }
  }
};
</script>

<style>
</style>
