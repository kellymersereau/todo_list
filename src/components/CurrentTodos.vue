<template>
  <div id="current-todos" class="flex-item">
    <h2>TO DO:</h2>
    <p v-if="todos.length === 0" class="italic">Add items above!</p>
    <ul class="list-group">
      <li class="list-group-item" v-for="todo in todos" v-bind:key="todo.id">
        {{ todo.body }}
        <div class="btn-group">
          <button type="button" @click="edit(todo)" class="btn">
            <span class="material-icons">edit</span>
          </button>
          <button type="button" @click="complete(todo)" class="btn">
            <span class="material-icons">done</span>
          </button>
          <button type="button" @click="remove(todo)" class="btn">
            <span class="material-icons">remove_circle_outline</span>
          </button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  methods: {
    edit(todo) {
      this.$store.dispatch("editTodo", todo);
    },
    complete(todo) {
      this.$store.dispatch("completeTodo", todo);
    },
    remove(todo) {
      this.$store.dispatch("removeTodo", todo);
    }
  },
  computed: {
    todos() {
      return this.$store.getters.todos;
    }
  }
};
</script>
<style>
.btn-group {
  float: right;
}
</style>
