<template>
  <div class="container">
    <div v-if="myRentals.length">
      <ClearMyItems />
      <MyItem v-for="item in myRentals" :key="item.id" :item="item" />
    </div>
    <div class="no-items container" v-else>
      <h2>No items here yet.</h2>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  layout: "no-nav",
  computed: {
    ...mapState(["myRentals"])
  }
};
</script>

<style scoped>
.no-items {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50vh;
}
</style>
