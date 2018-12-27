<template>
  <div id="app">
    <!--<img alt="Vue logo" src="./assets/logo.png">-->
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <h1 class="title">Todo List</h1>
    <list-items></list-items>
    <hr size="1">
    <add-item></add-item>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import AddItem from "./components/AddItem.vue";
import EditItem from "./components/EditItem.vue";
import ListItems from "./components/ListItems.vue";

export default {
  name: 'app',
  components: {
    AddItem,
    EditItem,
    ListItems
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
