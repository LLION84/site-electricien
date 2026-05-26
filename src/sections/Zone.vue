<template>
  <section id="zone" style="background: #1E2A3A; padding: 80px 24px; border-top: 3px solid #F59E0B;">
    <div style="max-width: 1200px; margin: 0 auto;">

      <div style="display: flex; align-items: center; gap: 10px; margin-bottom: 8px;">
        <div style="width: 3px; height: 16px; background: #F59E0B; border-radius: 2px;"></div>
        <span style="color: #F59E0B; font-size: 11px; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase;">Zone d'intervention</span>
      </div>

      <div class="zone-header">
        <h2 style="color: #F8F7F4; font-size: 32px; font-weight: 600; max-width: 480px; line-height: 1.2;">
          Nous intervenons pres de chez vous
        </h2>
        <p style="color: #9CA3AF; font-size: 14px; max-width: 340px; line-height: 1.7;">
          Base a Avignon, nous intervenons dans un rayon de 30km. Devis gratuit et sans engagement sous 24h.
        </p>
      </div>

      <div class="zone-content">

        <div class="zone-tags-wrap">
          <div v-for="ville in villes" :key="ville.nom" class="zone-tag">
            <span style="color: #F59E0B; font-size: 11px;">📍</span>
            <span>{{ ville.nom }}</span>
            <span style="color: #F59E0B; font-size: 11px; margin-left: auto;">{{ ville.km }}</span>
          </div>
        </div>

        <div class="zone-card">
          <div style="display: flex; align-items: center; gap: 10px; margin-bottom: 20px;">
            <div style="width: 3px; height: 16px; background: #F59E0B;"></div>
            <span style="color: #F8F7F4; font-size: 15px; font-weight: 600;">Intervention rapide</span>
          </div>
          <div style="display: flex; flex-direction: column; gap: 14px;">
            <div class="zone-info-row">
              <span style="color: #9CA3AF; font-size: 13px;">Delai d'intervention</span>
              <span style="color: #F59E0B; font-size: 13px; font-weight: 600;">Sous 24h</span>
            </div>
            <div style="height: 1px; background: rgba(255,255,255,0.06);"></div>
            <div class="zone-info-row">
              <span style="color: #9CA3AF; font-size: 13px;">Devis</span>
              <span style="color: #F59E0B; font-size: 13px; font-weight: 600;">Gratuit</span>
            </div>
            <div style="height: 1px; background: rgba(255,255,255,0.06);"></div>
            <div class="zone-info-row">
              <span style="color: #9CA3AF; font-size: 13px;">Disponibilite</span>
              <span style="color: #F59E0B; font-size: 13px; font-weight: 600;">Lun-Sam 8h-19h</span>
            </div>
            <div style="height: 1px; background: rgba(255,255,255,0.06);"></div>
            <div class="zone-info-row">
              <span style="color: #9CA3AF; font-size: 13px;">Rayon</span>
              <span style="color: #F59E0B; font-size: 13px; font-weight: 600;">30km autour Avignon</span>
            </div>
          </div>
          <a href="#contact" style="display: block; margin-top: 24px; background: #F59E0B; color: #111820; padding: 12px; font-size: 13px; font-weight: 600; text-align: center; text-decoration: none; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0 100%);">
            Demander un devis gratuit
          </a>
        </div>

      </div>

    </div>
  </section>
</template>

<script setup>
const villes = [
  { nom: 'Avignon', km: 'Centre' },
  { nom: 'Villeneuve-les-Avignon', km: '3 km' },
  { nom: 'Vedene', km: '7 km' },
  { nom: 'Montfavet', km: '5 km' },
  { nom: 'Chateaurenard', km: '15 km' },
  { nom: 'Cavaillon', km: '25 km' },
  { nom: 'L\'Isle-sur-la-Sorgue', km: '22 km' },
  { nom: 'Carpentras', km: '25 km' },
  { nom: 'Tarascon', km: '18 km' },
  { nom: 'Beaucaire', km: '22 km' },
]
</script>

<style scoped>
.zone-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 48px;
  flex-wrap: wrap;
  gap: 16px;
}

.zone-content {
  display: grid;
  grid-template-columns: 1fr 340px;
  gap: 24px;
  align-items: start;
}

.zone-tags-wrap {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
}

.zone-tag {
  display: flex;
  align-items: center;
  gap: 10px;
  background: #253447;
  border: 1px solid rgba(255,255,255,0.06);
  padding: 14px 16px;
  color: #D3D1C7;
  font-size: 13px;
  font-weight: 500;
  clip-path: polygon(0 0, 100% 0, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0 100%);
  transition: border-color 0.3s, background 0.3s;
}

.zone-tag:hover {
  border-color: #F59E0B;
  background: #2A3F55;
}

.zone-card {
  background: #253447;
  border: 1px solid rgba(245,158,11,0.2);
  padding: 24px;
  clip-path: polygon(0 0, 100% 0, 100% calc(100% - 14px), calc(100% - 14px) 100%, 0 100%);
}

.zone-info-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

@media (max-width: 768px) {
  .zone-content {
    grid-template-columns: 1fr;
  }

  .zone-tags-wrap {
    grid-template-columns: 1fr;
  }

  .zone-header {
    flex-direction: column;
    align-items: flex-start;
  }
}
</style>