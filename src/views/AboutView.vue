<template>
  <div class="about">
    <TodoComponent />
  </div>
</template>

<script>
import TodoComponent from "../components/TodoComponent.vue";
export default {
  name: "AboutTab",
  components: {
    TodoComponent,
  },
  data() {
    return {};
  },
};
</script>
