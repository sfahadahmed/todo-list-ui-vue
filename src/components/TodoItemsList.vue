<template>
    <div>
        <div>
            <form v-on:submit.prevent="add">
                <input type="text" name="todo" id="todo" v-model="todoText" placeholder="e.g. meeting at 10:00 AM">&nbsp;
                <button>Add</button>
            </form>
        </div>
        
        <div>
        <hr size="1">
        <ul style="text-align: left">
            <li
                v-for="(todoItem, index) in todoItems"
                v-bind:key="todoItem.id"
                v-bind:title="todoItem.title">
                {{todoItem.title}}
                &nbsp;
                <button v-on:click="remove(index)">Remove</button>
            </li>
        </ul>
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

</style>
