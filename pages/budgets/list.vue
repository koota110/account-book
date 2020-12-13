<template>
  <v-data-table
    :headers="headers">
  </v-data-table>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      headers:[
        {
          text:'Name',
          value:'name'
        }
      ]
    }
  }
})
</script>
