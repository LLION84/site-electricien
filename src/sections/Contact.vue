<template>
  <section id="contact" style="background: #F8F7F4; padding: 80px 24px; border-top: 3px solid #F59E0B;">
    <div style="max-width: 1200px; margin: 0 auto;">

      <div style="display: flex; align-items: center; gap: 10px; margin-bottom: 8px;">
        <div style="width: 3px; height: 16px; background: #F59E0B; border-radius: 2px;"></div>
        <span style="color: #F59E0B; font-size: 11px; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase;">Contact</span>
      </div>

      <div class="contact-header">
        <h2 style="color: #1E2A3A; font-size: 32px; font-weight: 600; max-width: 480px; line-height: 1.2;">
          Parlons de votre projet
        </h2>
        <p style="color: #6B7280; font-size: 14px; max-width: 340px; line-height: 1.7;">
          Devis gratuit sous 24h. Sans engagement. On vous rappelle quand vous voulez.
        </p>
      </div>

      <div class="contact-content">

        <div class="contact-infos">
          <div class="info-card">
            <div style="font-size: 20px;">📞</div>
            <div>
              <p style="color: #6B7280; font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 4px;">Telephone</p>
              <a href="tel:06XXXXXXXX" style="color: #1E2A3A; font-size: 18px; font-weight: 600; text-decoration: none;">06 XX XX XX XX</a>
            </div>
          </div>
          <div class="info-card">
            <div style="font-size: 20px;">⏰</div>
            <div>
              <p style="color: #6B7280; font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 4px;">Disponibilite</p>
              <p style="color: #1E2A3A; font-size: 15px; font-weight: 600;">Lun-Sam 8h-19h</p>
            </div>
          </div>
          <div class="info-card">
            <div style="font-size: 20px;">📍</div>
            <div>
              <p style="color: #6B7280; font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 4px;">Zone</p>
              <p style="color: #1E2A3A; font-size: 15px; font-weight: 600;">Avignon et 30km</p>
            </div>
          </div>
          <a href="tel:06XXXXXXXX" style="display: block; background: #F59E0B; color: #111820; padding: 14px; font-size: 14px; font-weight: 600; text-align: center; text-decoration: none; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0 100%);">
            Appeler maintenant
          </a>
          <p style="color: #9CA3AF; font-size: 12px; text-align: center;">Devis gratuit — reponse sous 24h</p>
        </div>

        <div class="contact-form">
          <h3 style="color: #1E2A3A; font-size: 16px; font-weight: 600; margin-bottom: 20px;">Envoyer un message</h3>
          <div style="display: flex; flex-direction: column; gap: 14px;">
            <div class="form-group">
              <label>Votre nom</label>
              <input type="text" placeholder="Marc Dupont" />
            </div>
            <div class="form-group">
              <label>Telephone</label>
              <input type="tel" placeholder="06 XX XX XX XX" />
            </div>
            <div class="form-group">
              <label>Votre besoin</label>
              <select>
                <option>Installation electrique</option>
                <option>Depannage urgent</option>
                <option>Tableau electrique</option>
                <option>Mise aux normes</option>
                <option>Eclairage</option>
                <option>Autre</option>
              </select>
            </div>
            <div class="form-group">
              <label>Message</label>
              <textarea rows="4" placeholder="Decrivez votre projet..."></textarea>
            </div>
            <button type="button" style="background: #1E2A3A; color: #F8F7F4; padding: 14px; font-size: 14px; font-weight: 600; border: none; cursor: pointer; clip-path: polygon(0 0, 100% 0, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0 100%); transition: background 0.3s;" @mouseenter="e => e.currentTarget.style.background = '#F59E0B'" @mouseleave="e => e.currentTarget.style.background = '#1E2A3A'">
              Envoyer ma demande
            </button>
          </div>
        </div>

      </div>

    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.contact-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 48px;
  flex-wrap: wrap;
  gap: 16px;
}

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
  align-items: start;
}

.contact-infos {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.info-card {
  display: flex;
  align-items: center;
  gap: 16px;
  background: white;
  border: 1px solid #E5E7EB;
  padding: 20px;
  clip-path: polygon(0 0, 100% 0, 100% calc(100% - 10px), calc(100% - 10px) 100%, 0 100%);
  transition: border-color 0.3s;
}

.info-card:hover {
  border-color: #F59E0B;
}

.contact-form {
  background: white;
  border: 1px solid #E5E7EB;
  padding: 32px;
  clip-path: polygon(0 0, 100% 0, 100% calc(100% - 14px), calc(100% - 14px) 100%, 0 100%);
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.form-group label {
  color: #1E2A3A;
  font-size: 13px;
  font-weight: 600;
}

.form-group input,
.form-group select,
.form-group textarea {
  background: #F8F7F4;
  border: 1px solid #E5E7EB;
  padding: 10px 14px;
  font-size: 13px;
  color: #1E2A3A;
  outline: none;
  font-family: inherit;
  transition: border-color 0.3s;
  clip-path: polygon(0 0, 100% 0, 100% calc(100% - 6px), calc(100% - 6px) 100%, 0 100%);
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  border-color: #F59E0B;
}

@media (max-width: 768px) {
  .contact-content {
    grid-template-columns: 1fr;
  }

  .contact-header {
    flex-direction: column;
    align-items: flex-start;
  }
}
</style>