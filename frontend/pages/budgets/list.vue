<template>
  <data-table :headers="headers" :items="budgets"> </data-table>
</template>
<script lang="ts">
import Vue from 'vue';
import DataTable from '~/components/molecules/dataTableWithPagenation.vue';
import { Header } from '~/types/globals/header';
import { Budget } from '~/types/budgets/budget';

export default Vue.extend({
  components: {
    DataTable,
  },
  data() {
    return {
      headers: [
        {
          text: 'Name',
          value: 'name',
        },
        {
          text: 'Author',
          value: 'author',
        },
        {
          text: 'CreatedAt',
          value: 'createdAt',
        },
        {
          text: 'LastUpdateTime',
          value: 'lastUpdateTime',
        },
      ] as Header[],
      budgets: [
        {
          name: '202012_予算',
          author: 'ohta',
          createdAt: new Date(),
          lastUpdateTime: new Date(),
        },
      ] as Budget[],
    };
  },
});
</script>
