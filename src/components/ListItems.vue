<template>
    <div id="list-items">
        <div class="card">
            <!--<img class="card-img-top" data-src="holder.js/100x180/?text=Image cap" alt="Card image cap">-->
            <!--<div class="card-body">
                <h4 class="card-title">Todo Items/h4>
                <p class="card-text">Text</p>
            </div>-->
            <ul class="list-group list-group-flush">
                <li v-for="item in todoItems" v-bind:key="item.id">{{item.text}}
                    <button type="button" name="" id="" class="btn btn-primary" btn-lg btn-block>Delete</button>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'list-items',
    props: ['items'],
    data: function(){
        return {
            todoItems: [
                {id: 0, text: "Apple"},
                {id: 1, text: "Strawberry"},
                {id: 2, text: "Grapes"}
            ]
        };
    }
}
</script>

<style>
#list-items {
    text-align: left;
}
</style>
