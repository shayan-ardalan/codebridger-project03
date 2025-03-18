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
  padding: 1.2rem;
  color: white;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

nav {
  display: flex;
  gap: 2rem;
  justify-content: center;
  max-width: 1200px;
  margin: 0 auto;
}

nav a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  transition: opacity 0.2s ease;
}

nav a:hover {
  opacity: 0.8;
}

main {
  min-height: calc(100vh - 120px);
  padding: 2rem 1rem;
}

.footer {
  background: var(--secondary-color);
  color: white;
  text-align: center;
  padding: 1.5rem;
  margin-top: 2rem;
}
</style> 