<template>
  <div>
    <div>
      <input
        v-model="todoMessage"
        type="text"
      >
      <button @click="add()">
        add
      </button>
    </div>
    <div>
      <ul>
        <li
          v-for="item in todo"
          :key="item.id"
        >
          {{ item.message }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "TodoComponent",
  data() {
    return {
      todo: [],
      todoMessage: "",
    };
  },
  watch: {
    todo() {
      console.log(this.todo);
    },
  },
  methods: {
    add() {
      this.todo = [
        ...this.todo,
        { id: Math.random() * 100, message: this.todoMessage },
      ];
      this.todoMessage = "";
    },
  },
};
</script>

<style></style>
