<template>
  <div class="container">
    <h1 class="main-title">قیمت‌های لحظه‌ای فارکس و داوجونز</h1>

    <div v-if="pending">در حال بارگذاری...</div>

    <div v-else-if="error">خطا در دریافت اطلاعات</div>

    <div v-else class="markets-grid">
      <div class="market-card" v-for="market in markets" :key="market.symbol">
        <h3>{{ market.name }}</h3>
        <p class="price">{{ market.price }}</p>
        <p class="change" :class="{ positive: market.change > 0, negative: market.change < 0 }">
          {{ market.change }}%
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
const markets = ref([
  { symbol: 'EUR/USD', name: 'یورو/دلار', price: '1.0892', change: 0.25 },
  { symbol: 'GBP/USD', name: 'پوند/دلار', price: '1.2654', change: -0.15 },
  { symbol: 'USD/JPY', name: 'دلار/ین', price: '149.32', change: 0.42 },
  { symbol: 'DOW', name: 'داوجونز', price: '38,791.35', change: 1.18 },
])

useHead({
  title: 'قیمت‌های لحظه‌ای فارکس و داوجونز'
})
</script>

<style scoped>
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

.main-title {
  text-align: center;
  color: var(--primary-color);
  margin-bottom: 2rem;
  font-size: 2.5rem;
}

.markets-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  padding: 1rem;
}

.market-card {
  background: white;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  text-align: center;
  transition: transform 0.2s ease;
}

.market-card:hover {
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