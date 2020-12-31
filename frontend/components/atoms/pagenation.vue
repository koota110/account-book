<template>
  <v-pagenation v-model="currentPage" :length="pageCount"> </v-pagenation>
</template>
<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  props: {
    page: {
      type: Number,
      required: true,
    },
    pageCount: {
      type: Number,
      required: true,
    },
  },
  data() {
    return {
      total: 10,
    };
  },
  computed: {
    value: {
      get(): Number {
        return this.page;
      },
      set(page: Number) {
        this.$emit('input', page);
      },
    },
  },
});
</script>
