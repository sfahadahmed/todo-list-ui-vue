<template>
    <div id="myroot" class="container">
        <div class="card">
            <div class="card-body">
                <form class="form-inline" v-on:submit.prevent="add">
                <div class="form-group">
                <label for="todo">Todo: </label>
                <input type="text" class="form-control" name="todo" id="todo" v-model="todoText" placeholder="e.g. meeting at 10:00 AM">&nbsp;
                <button class="btn btn-primary">Add</button>
                </div>
                </form>
            </div>
        </div>
        <hr size="1">
        <div class="card">
            <div class="card-body">
                <ul class="list-group" style="text-align: left">
                    <li class="list-group-item" 
                        v-for="(todoItem, index) in todoItems"
                        v-bind:key="todoItem.id"
                        v-bind:title="todoItem.title">
                        {{todoItem.title}}
                        &nbsp;
                        <button class="btn btn-warning" v-on:click="remove(index)">Remove</button>
                    </li>
                </ul>
                <span v-if="this.todoItems.length == 0">Add some todo items...</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'todo-items-list',
    data: function(){
        return { 
            todoText: '',
            todoCount: 0,
            todoItems: [],
        };
    },
    methods: {
        add: function(){
            this.todoItems.push({
                id: this.todoCount++,
                title: this.todoText
            });
        },
        remove: function(index){
            this.todoItems.splice(index,1);
            this.todoCount--;
        }
    }
}
</script>

<style>
.center {
    text-align: center;
}
</style>
