<template>
  <a v-if="visible" href="tel:06XXXXXXXX" class="float-btn">
    📞 Appeler maintenant
  </a>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const visible = ref(true)

const checkPosition = () => {
  const footer = document.querySelector('footer')
  if (!footer) return
  const rect = footer.getBoundingClientRect()
  visible.value = rect.top > window.innerHeight
}

onMounted(() => {
  window.addEventListener('scroll', checkPosition)
  checkPosition()
})

onUnmounted(() => {
  window.removeEventListener('scroll', checkPosition)
})
</script>

<style scoped>
.float-btn {
  display: none;
  position: fixed;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 100;
  background: #F59E0B;
  color: #111820;
  font-size: 14px;
  font-weight: 600;
  padding: 14px 32px;
  text-decoration: none;
  white-space: nowrap;
  clip-path: polygon(0 0, 100% 0, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0 100%);
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0% { box-shadow: 0 4px 20px rgba(245,158,11,0.4); }
  50% { box-shadow: 0 4px 30px rgba(245,158,11,0.7); }
  100% { box-shadow: 0 4px 20px rgba(245,158,11,0.4); }
}

@media (max-width: 768px) {
  .float-btn {
    display: block;
  }
}
</style>