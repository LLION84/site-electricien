<template>
  <section id="temoignages" style="background: #1E2A3A; padding: 80px 24px; border-top: 3px solid #F59E0B;">
    <div style="max-width: 1200px; margin: 0 auto;">

      <div style="display: flex; align-items: center; gap: 10px; margin-bottom: 8px;">
        <div style="width: 3px; height: 16px; background: #F59E0B; border-radius: 2px;"></div>
        <span style="color: #F59E0B; font-size: 11px; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase;">Temoignages</span>
      </div>

      <div class="temo-header">
        <h2 style="color: #F8F7F4; font-size: 32px; font-weight: 600; max-width: 480px; line-height: 1.2;">
          Ce que disent nos clients
        </h2>
        <div style="display: flex; align-items: center; gap: 8px;">
          <div style="display: flex; gap: 2px;">
            <span v-for="i in 5" :key="i" style="color: #F59E0B; font-size: 18px;">★</span>
          </div>
          <span style="color: #9CA3AF; font-size: 13px;">4.9/5 — 47 avis Google</span>
        </div>
      </div>

      <div class="temo-grid">
        <div v-for="temo in temoignages" :key="temo.nom" class="temo-card">
          <div style="display: flex; gap: 2px; margin-bottom: 12px;">
            <span v-for="i in temo.note" :key="i" style="color: #F59E0B; font-size: 14px;">★</span>
          </div>
          <p style="color: #D3D1C7; font-size: 14px; line-height: 1.7; margin-bottom: 20px; flex: 1;">
            "{{ temo.texte }}"
          </p>
          <div style="display: flex; align-items: center; gap: 12px; border-top: 1px solid rgba(255,255,255,0.06); padding-top: 16px;">
            <div style="width: 36px; height: 36px; background: rgba(245,158,11,0.15); border: 1px solid rgba(245,158,11,0.3); display: flex; align-items: center; justify-content: center; font-size: 14px; font-weight: 600; color: #F59E0B; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 6px), calc(100% - 6px) 100%, 0 100%);">
              {{ temo.nom[0] }}
            </div>
            <div>
              <p style="color: #F8F7F4; font-size: 13px; font-weight: 600;">{{ temo.nom }}</p>
              <p style="color: #6B7280; font-size: 12px;">{{ temo.ville }}</p>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
const temoignages = [
  {
    nom: 'Jean-Pierre M.',
    ville: 'Avignon',
    note: 5,
    texte: 'Intervention rapide pour une panne electrique. Serieux, propre et efficace. Je recommande sans hesiter.'
  },
  {
    nom: 'Sophie L.',
    ville: 'Vedene',
    note: 5,
    texte: 'Mise aux normes de notre tableau electrique faite dans les regles. Devis respecte, travail soigne. Parfait.'
  },
  {
    nom: 'Marc B.',
    ville: 'Chateaurenard',
    note: 5,
    texte: 'Tres professionnel. Installation complete pour notre maison neuve. Ponctuel et de bon conseil. Merci !'
  },
]
</script>

<style scoped>
.temo-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 48px;
  flex-wrap: wrap;
  gap: 16px;
}

.temo-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}

.temo-card {
  background: #253447;
  border: 1px solid rgba(255,255,255,0.06);
  padding: 28px;
  clip-path: polygon(0 0, 100% 0, 100% calc(100% - 14px), calc(100% - 14px) 100%, 0 100%);
  display: flex;
  flex-direction: column;
  transition: border-color 0.3s;
}

.temo-card:hover {
  border-color: #F59E0B;
}

@media (max-width: 768px) {
  .temo-grid {
    grid-template-columns: 1fr;
  }

  .temo-header {
    flex-direction: column;
    align-items: flex-start;
  }
}

@media (max-width: 1024px) and (min-width: 769px) {
  .temo-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>