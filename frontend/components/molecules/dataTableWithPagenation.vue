<template>
  <div>
    <data-table
      :headers="headers"
      :items="items"
      :page="page"
      :pageCount="pageCount"
    >
    </data-table>
    <pagenation v-model="page" :pageCount="pageCount"> </pagenation>
  </div>
</template>
<script lang="ts">
import Vue, { PropType } from 'vue';
import DataTable from '~/components/atoms/dataTable.vue';
import Pagenation from '~/components/atoms/pagenation.vue';
import { Header } from '~/types/globals/header';

export default Vue.extend({
  components: {
    DataTable,
    Pagenation,
  },
  props: {
    headers: {
      type: Array as PropType<Header[]>,
      required: true,
    },
    items: {
      type: Array as PropType<Object[]>,
      required: true,
    },
  },
  data() {
    return {
      page: 1,
      pageCount: 0,
    };
  },
});
</script>
