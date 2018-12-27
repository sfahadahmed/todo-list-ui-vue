<template>
    <div>
    <div class="form-group">
      <label for="item">Add todo item: </label>
      <input type="text" class="form-control" name="item" id="item" aria-describedby="helpId" placeholder="">&nbsp;
      <!--<small id="helpId" class="form-text text-muted">Todo item</small>-->
      <button type="button" name="add-button" id="add-button" class="btn btn-primary" btn-lg btn-block>Add Item</button>
    </div>
    </div>
</template>

<script>
export default {
    name: 'add-item',
    props: ['item']
}
</script>

<style>

</style>