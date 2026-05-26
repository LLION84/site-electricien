<template>
  <section id="home" style="background: #2A3F55; padding: 80px 24px 64px; min-height: 100vh; display: flex; align-items: center;">
    <div style="max-width: 1200px; margin: 0 auto; width: 100%; display: flex; align-items: center; gap: 48px; flex-wrap: wrap;">

      <div style="flex: 1; min-width: 300px;">
        <div style="display: inline-flex; align-items: center; background: rgba(245,158,11,0.12); color: #F59E0B; font-size: 11px; font-weight: 600; padding: 4px 14px; border-left: 3px solid #F59E0B; letter-spacing: 0.08em; text-transform: uppercase; margin-bottom: 24px;">
          Electricien agree RGE — Avignon
        </div>
        <h1 style="font-size: 42px; font-weight: 600; line-height: 1.2; margin-bottom: 16px; color: #F8F7F4;">
          Votre electricien<br>
          <span style="color: #F59E0B;">de confiance</span> a Avignon
        </h1>
        <p style="color: #9CA3AF; font-size: 16px; line-height: 1.7; margin-bottom: 32px;">
          Installation, depannage, mise aux normes. Intervention rapide sur Avignon et 30km autour. Devis gratuit sous 24h.
        </p>
        <div style="display: flex; gap: 12px; flex-wrap: wrap;">
          <a href="#contact" style="background: #F59E0B; color: #111820; padding: 12px 28px; font-size: 14px; font-weight: 600; text-decoration: none; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 10px), calc(100% - 10px) 100%, 0 100%);">
            Demander un devis
          </a>
          <a href="#services" style="border: 1px solid rgba(245,158,11,0.4); color: #F59E0B; padding: 12px 28px; font-size: 14px; font-weight: 500; text-decoration: none; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 10px), calc(100% - 10px) 100%, 0 100%);">
            Nos services
          </a>
        </div>
      <div style="display: inline-flex; align-items: center; gap: 12px; margin-top: 24px; background: rgba(245,158,11,0.08); border: 1px solid rgba(245,158,11,0.2); padding: 10px 18px; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0 100%);">
          <span style="color: #F59E0B; font-size: 16px; letter-spacing: 2px;">★★★★★</span>
          <div style="width: 1px; height: 16px; background: rgba(245,158,11,0.3);"></div>
          <span style="color: #F8F7F4; font-size: 13px; font-weight: 500;">4.9/5</span>
          <span style="color: #9CA3AF; font-size: 12px;">47 avis clients verifies</span>
        </div>
      </div>

      <div style="flex: 1; min-width: 300px; position: relative; padding-top: 32px;">
        <div style="position: absolute; top: 0; left: 50%; transform: translateX(-50%); z-index: 10; background: #111820; border: 2px solid #F59E0B; padding: 8px 16px; display: flex; align-items: center; gap: 8px; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0 100%); white-space: nowrap;">
          <span style="font-size: 20px;">{{ images[activeIndex].icon }}</span>
          <span style="color: #F59E0B; font-size: 12px; font-weight: 600; letter-spacing: 0.06em; text-transform: uppercase;">{{ images[activeIndex].label }}</span>
        </div>
        <div style="height: 460px; overflow: hidden; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 20px), calc(100% - 20px) 100%, 0 100%);">
          <swiper
            :modules="modules"
            :autoplay="{ delay: 3500, disableOnInteraction: false }"
            :loop="true"
            :effect="'fade'"
            style="width: 100%; height: 100%;"
            @slideChange="onSlideChange"
          >
            <swiper-slide v-for="(img, index) in images" :key="index">
              <div style="width: 100%; height: 100%; position: relative;">
                <img :src="img.url" :alt="img.label" style="width: 100%; height: 100%; object-fit: cover;" />
                <div style="position: absolute; inset: 0; background: rgba(17,24,32,0.3);"></div>
              </div>
            </swiper-slide>
          </swiper>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Autoplay, EffectFade } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/effect-fade'

const modules = [Autoplay, EffectFade]
const activeIndex = ref(0)

const images = [
  { url: 'https://images.unsplash.com/photo-1621905251189-08b45d6a269e?w=800&q=80', label: 'Depannage', icon: '🔧' },
  { url: 'https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=800&q=80', label: 'Installation', icon: '⚡' },
  { url: 'https://images.unsplash.com/photo-1473341304170-971dccb5ac1e?w=800&q=80', label: 'Tableau electrique', icon: '📋' },
  { url: 'https://images.unsplash.com/photo-1504328345606-18bbc8c9d7d1?w=800&q=80', label: 'Mise aux normes', icon: '✅' },
]

const onSlideChange = (swiper) => {
  activeIndex.value = swiper.realIndex
}
</script>