<template>
  <div style="background: #1E2A3A; min-height: 100vh;">
    <Header />
    <Hero />
    <Services />
    <Zone />
    <Contact />
    <Footer />
    <FloatButton />
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import Hero from './sections/Hero.vue'
import Services from './sections/Services.vue'
import Zone from './sections/Zone.vue'
import Contact from './sections/Contact.vue'
import Footer from './components/Footer.vue'
import FloatButton from './components/FloatButton.vue'
</script>