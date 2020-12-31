<template>
  <v-data-table
    :headers="headers"
    :items="items"
    :height="height"
    :item-key="key"
    :items-per-page="itemsPerPage"
    fixed-header
    hide-default-footer
    class="elevation-1"
    :page.sync="page"
    @page-count="pageCount = $event"
  >
  </v-data-table>
</template>
<script lang="ts">
import Vue, { PropType } from 'vue';
import { Header } from '~/types/globals/header';

export default Vue.extend({
  props: {
    headers: {
      type: Array as PropType<Header[]>,
      required: true,
    },
    items: {
      type: Array as PropType<Object[]>,
      required: true,
    },
    height: {
      type: String,
      required: false,
      default: '400px',
    },
    key: {
      type: String,
      required: false,
      default: "id"
    },
    itemsPerPage: {
      type: Number,
      required: false,
      default: 15,
    },
    page: {
      type: Number,
      required: false,
      default: 1
    },
    pageCount: {
      type: Number,
      required: false,
      default: 0
    }
  },
});
</script>
