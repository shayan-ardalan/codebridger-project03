<template>
  <div class="price-card">
    <h3>{{ symbol }}</h3>
    <p class="price">{{ price }}</p>
    <p class="change" :class="{ positive: change > 0, negative: change < 0 }">
      {{ change }}%
    </p>
  </div>
</template>

<script setup>
defineProps({
  symbol: String,
  price: Number,
  change: Number
})
</script>

<style scoped>
.price-card {
  background: white;
  padding: 1rem;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  text-align: center;
}

.price {
  font-size: 1.5rem;
  font-weight: bold;
  margin: 0.5rem 0;
}

.positive {
  color: green;
}

.negative {
  color: red;
}
</style> 