<template>
  <div class="container">
    <h1 class="main-title">قیمت‌های لحظه‌ای</h1>

    <div v-if="pending">در حال بارگذاری...</div>

    <div v-else-if="error">خطا در دریافت اطلاعات</div>

    <div v-else class="prices-grid">
      <PriceCard
        v-for="coin in data"
        :key="coin.symbol"
        v-bind="coin"
      />
    </div>
  </div>
</template>

<script setup>

const { data, pending, error } = await useFetch('/api/prices')

useHead({
  title: 'قیمت‌های لحظه‌ای '
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

.prices-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
  padding: 1rem;
}
</style> 