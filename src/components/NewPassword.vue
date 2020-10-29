<template>
  <div class="col-md-3 offset-2 shadow p-3 mb-5 bg-white rounded">
    <h4>FORM</h4>
    <hr>
    <form>
      <div class="form-group">
        <label>username or email (optional)</label>
        <input type="text" v-model="form.username" class="form-control">
      </div>
      <div class="form-group">
        <label>password</label>
        <input type="password" v-model="form.password" class="form-control">
      </div>
      <div class="form-group">
        <label>select platform</label>
        <select class="form-control" v-model="form.platform">
          <option v-for="item in itemList" :key="item">{{ item }}</option>
        </select>
      </div>
      <div class="form-group">
        <button class="btn btn-success btn-sm" @click="onSaveForm" type="button">SAVE</button>
      </div>
    </form>
  </div>
</template>

<script>
  import { eventBus } from "@/main";

  export default {
    data: function() {
      return{
        itemList: [
            "Netflix",
            "Spotify",
            "Youtube",
            "Google",
            "Linkedin"
        ],
        form: {
          username: '',
          password: '',
          platform: 'Netflix',
        }
      }
    },
    methods: {
      onSaveForm() {
        eventBus.$emit('saveForm', this.form);
        this.form = {
          username: '',
          password: '',
          platform: 'Netflix',
        }
      }
    }
  }
</script>
