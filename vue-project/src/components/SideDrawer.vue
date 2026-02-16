<script setup lang="ts">
import { ref } from 'vue'
import { RouterLink, useRouter } from 'vue-router'

const isOpen = ref(false)
const router = useRouter()

function toggle() {
  isOpen.value = !isOpen.value
}

function close() {
  isOpen.value = false
}

router.afterEach(() => {
  close()
})
</script>

<template>
  <button class="hamburger" :class="{ open: isOpen }" @click="toggle" aria-label="Toggle menu">
    <span></span>
    <span></span>
    <span></span>
  </button>

  <Transition name="overlay">
    <div v-if="isOpen" class="overlay" @click="close"></div>
  </Transition>

  <Transition name="drawer">
    <nav v-if="isOpen" class="drawer">
      <div class="drawer-header">Menu</div>
      <RouterLink to="/" class="drawer-link">Home</RouterLink>
      <RouterLink to="/about" class="drawer-link">About</RouterLink>
      <RouterLink to="/services" class="drawer-link">Services</RouterLink>
      <RouterLink to="/contact" class="drawer-link">Contact</RouterLink>
    </nav>
  </Transition>
</template>

<style scoped>
.hamburger {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 5px;
  width: 36px;
  height: 36px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 4px;
  z-index: 1001;
  position: relative;
}

.hamburger span {
  display: block;
  width: 100%;
  height: 2px;
  background-color: var(--color-heading);
  border-radius: 2px;
  transition: transform 0.3s ease, opacity 0.3s ease;
  transform-origin: center;
}

.hamburger.open span:nth-child(1) {
  transform: translateY(7px) rotate(45deg);
}

.hamburger.open span:nth-child(2) {
  opacity: 0;
}

.hamburger.open span:nth-child(3) {
  transform: translateY(-7px) rotate(-45deg);
}

.overlay {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.5);
  z-index: 999;
}

.drawer {
  position: fixed;
  top: 0;
  left: 0;
  width: 260px;
  height: 100vh;
  background: var(--color-background-soft);
  z-index: 1000;
  display: flex;
  flex-direction: column;
  padding-top: 1rem;
  box-shadow: 2px 0 12px rgba(0, 0, 0, 0.3);
}

.drawer-header {
  color: var(--color-heading);
  font-size: 1.25rem;
  font-weight: 600;
  padding: 1rem 1.5rem;
  border-bottom: 1px solid var(--color-border);
  margin-bottom: 0.5rem;
}

.drawer-link {
  display: block;
  padding: 0.75rem 1.5rem;
  color: var(--color-text);
  font-size: 1rem;
  transition: background-color 0.2s;
}

.drawer-link:hover {
  background-color: var(--color-background-mute);
}

.drawer-link.router-link-exact-active {
  color: hsla(160, 100%, 37%, 1);
  background-color: var(--color-background-mute);
}

/* Transitions */
.overlay-enter-active,
.overlay-leave-active {
  transition: opacity 0.3s ease;
}

.overlay-enter-from,
.overlay-leave-to {
  opacity: 0;
}

.drawer-enter-active,
.drawer-leave-active {
  transition: transform 0.3s ease;
}

.drawer-enter-from,
.drawer-leave-to {
  transform: translateX(-100%);
}
</style>
