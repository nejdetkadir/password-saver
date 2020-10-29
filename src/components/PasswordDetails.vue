<template>
  <div v-if="password !== ''">
    <hr>
    <div class="row">
      <div class="col-md-8 mx-auto">
        <div class="alert alert-primary" role="alert">
          {{ username }} | {{ password }}
        </div>
        <button class="btn btn-warning btn-sm" @click="password=''">hide</button>
      </div>
    </div>
    <hr>
  </div>
</template>

<script>
  import { eventBus } from "@/main";

  export default {
    data: function() {
      return{
        username: '',
        password: ''
      }
    },
    created() {
      eventBus.$on('showDetails', (data) => {
        this.status = true;
        this.username = data.username;
        this.password = data.password;
      });
    }
  }
</script>
