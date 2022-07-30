<template>
  <div>
    <div>My name is {{ name }}</div>
    <div>this is my first component</div>
    <button @click="increatment()">
      increase
    </button>
    <div>{{ count }}</div>
    <div>{{ reverseName }}</div>
    <div>
      <input
        v-model="name"
        type="text"
      >
    </div>
    <div>
      <input
        v-model="message"
        type="text"
      >
    </div>
    <div>method:{{ nameMethod() }}</div>
  </div>
</template>
<script>

export default {
  name: "FirstComponent",
  data() {
    return {
      name: "Prasun Mukherjee",
      count: 0,
      message: "",
    };
  },
  computed: {
    reverseName: function () {
      console.log("reverseName called.");
      return this.name.split("").reverse().join("");
    },
  },
  watch:{
    message(){
        console.log('watching message..');
    }
  },
  methods: {
    increatment() {
      this.count++;
    },
    nameMethod() {
        console.log("method calling...");
      return this.name;
    },
  }
};
</script>
