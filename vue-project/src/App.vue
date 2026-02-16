<script setup lang="ts">
import { RouterView } from 'vue-router'
import SideDrawer from './components/SideDrawer.vue'
</script>

<template>
  <div class="app-layout">
    <header class="top-bar">
      <SideDrawer />
      <span class="site-title">My Vue App</span>
    </header>

    <RouterView />
  </div>
</template>

<style scoped>
.app-layout {
  min-height: 100vh;
}

.top-bar {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 0.75rem 1.5rem;
  background: var(--color-background-soft);
  border-bottom: 1px solid var(--color-border);
  position: sticky;
  top: 0;
  z-index: 100;
}

.site-title {
  color: var(--color-heading);
  font-size: 1.15rem;
  font-weight: 600;
}
</style>
