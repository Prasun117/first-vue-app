<template>
  <div >
    <button @click="$emit('addEvent',5)">click me!</button>
  </div>
</template>

<script>
export default {
  name: "increment-component",
  props: {

  },
  methods: {},
};
</script>
