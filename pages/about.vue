<template>
  <div class="container">
    <h1 class="main-title">درباره ما</h1>
    <div class="about-content">
      <p>ما یک پلتفرم تخصصی در زمینه ارائه اطلاعات و تحلیل‌های بازار فارکس و شاخص داوجونز هستیم.</p>
      <p>هدف ما کمک به معامله‌گران برای اتخاذ تصمیمات هوشمندانه در بازارهای مالی جهانی است.</p>
      
      <div class="features">
        <div class="feature-card">
          <h3>بازار فارکس</h3>
          <p>بزرگترین بازار مالی جهان با گردش مالی روزانه بیش از 6 تریلیون دلار</p>
        </div>
        <div class="feature-card">
          <h3>شاخص داوجونز</h3>
          <p>معتبرترین شاخص بازار سهام آمریکا شامل 30 شرکت برتر</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.about-content {
  max-width: 800px;
  margin: 0 auto;
  line-height: 1.8;
  text-align: center;
}

.features {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 3rem;
}

.feature-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
}

.feature-card h3 {
  color: var(--primary-color);
  margin-bottom: 1rem;
}
</style> 