<template>
  <div>
    <b-button
      class="mt-3"
      variant="outline-danger"
      @click="
        () => {
          clearMyItems();
        }
      "
      >Clear All</b-button
    >
  </div>
</template>

<script>
import { mapMutations } from "vuex";
export default {
  methods: {
    ...mapMutations(["clearMyItems"])
  }
};
</script>

<style scoped></style>
