<template>
  <nuxt-link :to="`/products/${card.id}`" class="card">
    <img
      :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)"
      alt="fe"
      class="image"
    />
    <h3 class="header">{{ card.title }}</h3>
    <p class="snippet">{{ card.snippet }}</p>
  </nuxt-link>
</template>

<script>
export default {
  props: ["card"]
};
</script>

<style scoped>
.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
  text-decoration: none;
}

.card .image {
  transition: 0.3s ease;
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}

.card:hover .image {
  transform: translateY(-10px);
  transition: transform 0.3s ease;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
  color: #000;
}
.header:hover {
  color: #000;
  text-decoration: none;
}
.snippet {
  color: grey;
}
</style>
