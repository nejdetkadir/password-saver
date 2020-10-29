<template>
  <div class="col-md-3 offset-2 shadow p-3 mb-5 bg-white rounded">
    <h4>LIST</h4>
    <hr>
    <ul class="list-group">
      <PasswordElement v-for="item in passList" :key="item.id">
        <li class="list-group-item" :id="item.id" @click="showDetails($event)">{{ item.platform }}</li>
      </PasswordElement>
    </ul>
  </div>
</template>

<script>
  import PasswordElement from "@/components/PasswordElement";
  import { eventBus } from "@/main";

  export default {
    components: {
      PasswordElement
    },
    data: function() {
      return{
        passList: []
      }
    },
    methods: {
      showDetails(e) {
        eventBus.$emit('showDetails', this.passList[e.target.id-1]);
      }
    },
    created() {
      eventBus.$on('saveForm', (data) => {
        this.passList.push({id: this.passList.length+1, ...data});
      });
    }
  }
</script>
