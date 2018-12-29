<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1 class="title">Todo List</h1>
    <todo-items-list></todo-items-list>   
  </div>
</template>

<script>
import TodoItemsList from "./components/TodoItemsList.vue";

export default {
  name: 'app',
  components: {
    TodoItemsList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#title {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  font-size: larger;
}


</style>
