<template>
  <div id="completed-todos" class="flex-item">
    <h2>COMPLETED:</h2>
    <p v-if="completed.length === 0" class="italic">Nothing to show!</p>
    <ul class="list-group">
      <li
        class="list-group-item"
        v-for="todo in completed"
        v-bind:key="todo.id"
      >
        {{ todo.body }}
        <button type="button" @click="remove(todo)" class="btn">
          <i class="material-icons purple">delete</i>
        </button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  methods: {
    remove(todo) {
      this.$store.dispatch("removeTodo", todo);
    }
  },
  computed: {
    completed() {
      return this.$store.getters.completedTodos;
    }
  }
};
</script>
