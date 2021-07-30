<template>
  <nuxt-link :to="`/products/${card.id}`" class="card-container">
    <img
      class="image"
      :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)"
      alt="fe"
    />
  </nuxt-link>
</template>

<script>
export default {
  props: ["card"]
};
</script>

<style scoped>
.card-container {
  width: 24%;
  height: 12.5rem;
  border-radius: 0.5rem;
  overflow: hidden;
  margin-bottom: 1.5rem;
  cursor: pointer;
}
.image {
  width: 100%;
  height: 100%;
  border-radius: 0.5rem;
  transition: 0.3s ease;
}

.image:hover {
  transform: translateY(-10px);
  transition: transform 0.3s ease;
}
</style>
