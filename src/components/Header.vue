<template>
  <header style="background: #111820; border-bottom: 1px solid rgba(255,255,255,0.08); box-shadow: 0 2px 20px rgba(0,0,0,0.5); position: fixed; top: 0; left: 0; width: 100%; z-index: 50;">
    <div style="max-width: 1200px; margin: 0 auto; padding: 0 24px; height: 56px; display: flex; align-items: center; justify-content: space-between;">

      <a href="#home" style="color: #F59E0B; font-weight: 600; font-size: 15px; text-decoration: none;">
        Dupont Electricite
      </a>

      <nav class="desktop-nav" style="display: flex; align-items: center; gap: 24px;">
        <a href="#services" style="color: #9CA3AF; font-size: 13px; text-decoration: none;">Services</a>
        <a href="#zone" style="color: #9CA3AF; font-size: 13px; text-decoration: none;">Zone</a>
        <a href="#contact" style="color: #9CA3AF; font-size: 13px; text-decoration: none;">Contact</a>
        <a href="#contact" style="background: #F59E0B; color: #111820; padding: 8px 18px; font-size: 13px; font-weight: 600; text-decoration: none; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0 100%);">
          Nous appeler
        </a>
      </nav>

      <button @click="menuOpen = !menuOpen" class="burger" style="display: none; flex-direction: column; justify-content: space-between; width: 24px; height: 16px; background: none; border: none; cursor: pointer; padding: 0;">
        <span :style="{ display: 'block', width: '100%', height: '2px', background: '#D3D1C7', transition: 'all 0.3s', transform: menuOpen ? 'translateY(7px) rotate(45deg)' : 'none' }"></span>
        <span :style="{ display: 'block', width: '100%', height: '2px', background: '#D3D1C7', transition: 'all 0.3s', opacity: menuOpen ? 0 : 1 }"></span>
        <span :style="{ display: 'block', width: '100%', height: '2px', background: '#D3D1C7', transition: 'all 0.3s', transform: menuOpen ? 'translateY(-7px) rotate(-45deg)' : 'none' }"></span>
      </button>

    </div>

    <div v-if="menuOpen" style="display: flex; flex-direction: column; align-items: center; gap: 20px; padding: 24px; background: #111820; border-top: 1px solid rgba(255,255,255,0.05);">
      <a href="#services" @click="menuOpen = false" style="color: #9CA3AF; font-size: 14px; text-decoration: none;">Services</a>
      <a href="#zone" @click="menuOpen = false" style="color: #9CA3AF; font-size: 14px; text-decoration: none;">Zone</a>
      <a href="#contact" @click="menuOpen = false" style="color: #9CA3AF; font-size: 14px; text-decoration: none;">Contact</a>
      <a href="#contact" @click="menuOpen = false" style="background: #F59E0B; color: #111820; padding: 10px 24px; font-size: 13px; font-weight: 600; text-decoration: none; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0 100%);">
        Nous appeler
      </a>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
const menuOpen = ref(false)
</script>

<style scoped>
@media (max-width: 768px) {
  .desktop-nav { display: none !important; }
  .burger { display: flex !important; }
}
</style>