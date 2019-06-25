<template>
  <div id="app" class="wrapper">
    <CompletedTodos></CompletedTodos>
    <GetTodo></GetTodo>
    <CurrentTodos></CurrentTodos>
  </div>
</template>

<script>
import GetTodo from "./components/GetTodo.vue";
import CurrentTodos from "./components/CurrentTodos.vue";
import CompletedTodos from "./components/CompletedTodos.vue";
export default {
  components: {
    GetTodo,
    CurrentTodos,
    CompletedTodos
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
