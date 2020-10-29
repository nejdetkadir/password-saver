<template>
  <div class="col-md-3 offset-2 shadow p-3 mb-5 bg-white rounded">
    <h4>FORM</h4>
    <hr>
    <form>
      <div class="form-group">
        <label>username or email (optional)</label>
        <input type="text" class="form-control">
      </div>
      <div class="form-group">
        <label>password</label>
        <input type="password" class="form-control">
      </div>
      <div class="form-group">
        <label for="exampleFormControlSelect1">select platform</label>
        <select class="form-control" id="exampleFormControlSelect1">
          <option>1</option>
        </select>
      </div>
      <div class="form-group">
        <button class="btn btn-success btn-sm">SAVE</button>
      </div>
    </form>
  </div>
</template>

<script>
  export default {
  }
</script>
