<template>
    <div>

    <div class="form-group">
      <label for="item">Todo</label>
      <input type="text" class="form-control" name="item" id="item" aria-describedby="helpId" placeholder="">
      <!--<small id="helpId" class="form-text text-muted">Todo item</small>-->
    </div>

    <button type="button" name="update-button" id="update-button" class="btn btn-primary" btn-lg btn-block>Update Item</button>
   
    </div>
</template>

<script>
export default {
    name: 'edit-item',
    props: ['item']
}
</script>

<style>

</style>
