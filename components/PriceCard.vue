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
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  text-align: center;
  transition: transform 0.2s ease;
}

.price-card:hover {
  transform: translateY(-5px);
}

.price {
  font-size: 1.8rem;
  font-weight: bold;
  margin: 0.8rem 0;
  color: var(--primary-color);
}

.positive {
  color: #2ecc71;
}

.negative {
  color: #e74c3c;
}
</style> 