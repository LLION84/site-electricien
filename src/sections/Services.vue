<template>
  <section id="services" style="background: #F8F7F4; padding: 80px 24px; border-top: 3px solid #F59E0B;">
    <div style="max-width: 1200px; margin: 0 auto;">

      <div style="display: flex; align-items: center; gap: 10px; margin-bottom: 8px;">
        <div style="width: 3px; height: 16px; background: #F59E0B; border-radius: 2px;"></div>
        <span style="color: #F59E0B; font-size: 11px; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase;">Nos services</span>
      </div>

      <div class="services-header">
        <h2 style="color: #1E2A3A; font-size: 32px; font-weight: 600; max-width: 480px; line-height: 1.2;">
          Des solutions electriques pour chaque besoin
        </h2>
        <div style="display: flex; gap: 10px; flex-wrap: wrap;">
          <div class="badge">✓ Agree RGE</div>
          <div class="badge">✓ Devis gratuit</div>
          <div class="badge">✓ Intervention 7j/7</div>
        </div>
      </div>

      <div class="services-grid">
        <div
          v-for="(service, index) in services"
          :key="service.nom"
          class="service-card"
          style="background: #F0EEE8; padding: 28px; display: flex; gap: 20px; align-items: flex-start; position: relative; overflow: hidden;"
        >
          <div style="width: 48px; height: 48px; background: rgba(245,158,11,0.1); border: 1px solid rgba(245,158,11,0.3); display: flex; align-items: center; justify-content: center; flex-shrink: 0; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0 100%);">
            <span style="color: #F59E0B; font-size: 20px;">{{ service.icon }}</span>
          </div>
          <div>
            <h3 style="color: #1E2A3A; font-size: 15px; font-weight: 600; margin-bottom: 8px;">{{ service.nom }}</h3>
            <p style="color: #6B7280; font-size: 13px; line-height: 1.6;">{{ service.desc }}</p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
const services = [
  { icon: '⚡', nom: 'Installation electrique', desc: 'Travaux neufs et renovation pour maison, appartement et local commercial.' },
  { icon: '🔧', nom: 'Depannage urgent', desc: 'Intervention rapide 7j/7 sur panne, court-circuit et disjoncteur.' },
  { icon: '📋', nom: 'Tableau electrique', desc: 'Remplacement, mise aux normes et verification complete.' },
  { icon: '✅', nom: 'Mise aux normes', desc: 'Diagnostic et certification de vos installations electriques.' },
  { icon: '💡', nom: 'Eclairage', desc: 'Spots, LED, eclairage exterieur et solutions domotiques.' },
  { icon: '🏠', nom: 'Renovation', desc: 'Remise a neuf complete de votre installation electrique.' },
]
</script>

<style scoped>
.services-header {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  margin-bottom: 48px;
  flex-wrap: wrap;
  gap: 16px;
}

.badge {
  background: rgba(245,158,11,0.1);
  border: 1px solid rgba(245,158,11,0.2);
  padding: 6px 14px;
  color: #F59E0B;
  font-size: 11px;
  font-weight: 600;
  clip-path: polygon(0 0, 100% 0, 100% calc(100% - 6px), calc(100% - 6px) 100%, 0 100%);
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 16px;
}

.service-card {
  clip-path: polygon(0 0, 100% 0, 100% calc(100% - 14px), calc(100% - 14px) 100%, 0 100%);
  transition: transform 0.3s, outline-color 0.3s;
  outline: 1px solid #9CA3AF;
}

.service-card:hover {
  transform: translateY(-4px);
  outline: 1px solid #F59E0B;
}

.service-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, transparent, #F59E0B, transparent);
  opacity: 0;
  transition: opacity 0.4s ease;
}

.service-card::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, transparent, #F59E0B, transparent);
  opacity: 0;
  transition: opacity 0.4s ease;
}

.service-card:hover::before,
.service-card:hover::after {
  opacity: 1;
}

@media (max-width: 768px) {
  .services-grid {
    grid-template-columns: 1fr;
  }

  .services-header {
    flex-direction: column;
    align-items: flex-start;
  }
}

@media (max-width: 1024px) and (min-width: 769px) {
  .services-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>