<template>
  <div id="app" class="wrapper">
    <h1 class="header">
      To-do list
    </h1>
    <p class="header-copy center">
      Type into the box below and click the "+" to add items to the to-do list.
    </p>
    <GetTodo></GetTodo>
    <div class="flex-wrapper">
      <CurrentTodos></CurrentTodos>
      <CompletedTodos></CompletedTodos>
    </div>
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
  font-family: "Open Sans", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #100b21;
}
.header {
  font-size: 4em;
  text-align: center;
  color: #100b21;
  border-bottom: 1px solid #585a9c;
  margin: 0;
  padding: 20px;
}
.header-copy {
  width: 65%;
  margin: 0 auto;
  padding-top: 30px;
  padding-bottom: 10px;
  font-size: 1em;
  color: #5a5a5a;
}
.btn {
  border: none;
  background: transparent;
}
.material-icons {
  &.purple {
    color: #251950;
  }
}
.flex-wrapper {
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-between;
  align-content: flex-start;
  align-items: flex-start;
  box-sizing: border-box;
  margin: 20px auto;
  border: 1px solid #afafaf;
  box-shadow: #cbcbcb 2px 2px 5px;
  max-width: 95%;
  .flex-item {
    flex: 0 0 50%;
    box-sizing: border-box;
    height: 100%;
    &:first-of-type {
      border-right: 1px solid #afafaf;
      h2 {
        background-color: #10a487;
        border-bottom: #afafaf;
      }
    }
    &:last-of-type {
      h2 {
        background-color: #585a9c;
        border-bottom: #afafaf;
      }
      li {
        text-decoration: line-through;
        color: #919191;
      }
    }
    h2 {
      margin: 0;
      padding: 20px;
      font-size: 2em;
      font-weight: bold;
      color: #fdfdff;
    }
    p {
      padding: 20px;
      margin: 0;
    }
  }
}
p {
  &.italic {
    font-style: italic;
  }
}
ul {
  padding: 0;
  margin: 0;
  list-style: none;
  li {
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-between;
    align-items: center;
    align-content: center;
    padding: 20px;
    border-top: 1px solid #afafaf;
    text-align: left;
    &:first-of-type {
      border-top: none;
    }
    .btn-group {
      flex: 0 0 31%;
      btn {
        padding: 0 5px;
      }
    }
  }
}

.container {
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
  align-items: center;
  align-content: center;
  padding: 20px;
  input {
    border: 1px solid #4d4d4d;
    color: #100b21;
    font-size: 1.25em;
    padding: 10px 10px;
    flex: 0 0 60%;
    &:focus {
      outline: none;
      border: 2px solid #7fa97f;
    }
  }
  .btn {
    padding: 5px 10px;
    vertical-align: middle;
    span {
      font-size: 2.75em;
    }
  }
}
</style>
