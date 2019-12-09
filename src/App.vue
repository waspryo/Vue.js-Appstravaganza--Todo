<template>
  <div id="app" class="container">
    <h1 class="text-center">todo App</h1>
    <form @submit.prevent="addTodo()">
      <div class="form-group">
        <label for="newTodo">New Todo</label>
        <input
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
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {};
  },
  methods: {
    addTodo() {
      console.log('form submitted')
    }
  }
};
</script>

<style>
</style>
