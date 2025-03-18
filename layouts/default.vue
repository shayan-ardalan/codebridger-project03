<template>
  <div>
    <header class="header">
      <nav>
        <NuxtLink to="/">خانه</NuxtLink>
        <NuxtLink to="/about">درباره</NuxtLink>
        <NuxtLink to="/contact">تماس</NuxtLink>
      </nav>
    </header>

    <main>
      <slot />
    </main>

    <footer class="footer">
      <p>تمامی حقوق محفوظ است</p>
    </footer>
  </div>
</template>

<style scoped>
.header {
  background: var(--primary-color);
  padding: 1rem;
  color: white;
}

nav {
  display: flex;
  gap: 1rem;
  justify-content: center;
}

nav a {
  color: white;
  text-decoration: none;
}

.footer {
  background: var(--secondary-color);
  color: white;
  text-align: center;
  padding: 1rem;
  margin-top: 2rem;
}
</style> 