<template>
  <div>
    <div>{{ count }}</div>
    <IncrementComponent @addEvent="addEvent" />
    <download-csv></download-csv>
  </div>
</template>
<script>
import IncrementComponent from "../components/IncrementComponent.vue";
import DownloadCsv from '../components/DownloadCsv.vue'
export default {
  name: "PocView",
  data() {
    return {
      data: [],
      count: 0,
    };
  },
  components: {
    IncrementComponent,
    DownloadCsv
  },
  methods: {
    addEvent: function (incrementBy) {
      this.count += incrementBy;
    },
  },
};
</script>
