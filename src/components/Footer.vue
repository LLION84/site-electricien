<template>
  <footer style="background: #111820; border-top: 3px solid #F59E0B; padding: 48px 24px 24px;">
    <div style="max-width: 1200px; margin: 0 auto;">

      <div class="footer-grid">

        <div style="display: flex; flex-direction: column; gap: 12px;">
          <span style="color: #F59E0B; font-size: 18px; font-weight: 600;">Dupont Electricite</span>
          <p style="color: #6B7280; font-size: 13px; line-height: 1.7; max-width: 260px;">
            Electricien agree RGE a Avignon. Intervention rapide sur Avignon et 30km autour.
          </p>
          <a href="tel:06XXXXXXXX" style="display: inline-flex; align-items: center; gap: 8px; color: #F59E0B; font-size: 14px; font-weight: 600; text-decoration: none; margin-top: 4px;">
            📞 06 XX XX XX XX
          </a>
        </div>

        <div style="display: flex; flex-direction: column; gap: 12px;">
          <p style="color: #F8F7F4; font-size: 12px; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase;">Navigation</p>
          <a href="#home" class="footer-link">Accueil</a>
          <a href="#services" class="footer-link">Services</a>
          <a href="#zone" class="footer-link">Zone d'intervention</a>
          <a href="#contact" class="footer-link">Contact</a>
        </div>

        <div style="display: flex; flex-direction: column; gap: 12px;">
          <p style="color: #F8F7F4; font-size: 12px; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase;">Certifications</p>
          <div class="cert-badge">✓ Agree RGE</div>
          <div class="cert-badge">✓ Assure decennale</div>
          <div class="cert-badge">✓ Devis gratuit</div>
          <div class="cert-badge">✓ Intervention 7j/7</div>
        </div>

        <div style="display: flex; flex-direction: column; gap: 12px;">
          <p style="color: #F8F7F4; font-size: 12px; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase;">Mentions legales</p>
          <span style="color: #6B7280; font-size: 13px;">Dupont Electricite</span>
          <span style="color: #6B7280; font-size: 13px;">SIRET : XXXXXXXXXXXXXX</span>
          <span style="color: #6B7280; font-size: 13px;">Avignon, France</span>
        </div>

      </div>

      <div style="border-top: 1px solid rgba(255,255,255,0.05); margin-top: 40px; padding-top: 20px; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 12px;">
        <span style="color: #444441; font-size: 12px;">2025 Dupont Electricite — Tous droits reserves</span>
        <a href="https://zinne.fr" style="color: #F59E0B; font-size: 12px; font-weight: 500; text-decoration: none;">Propulse par Zinne</a>
      </div>

    </div>
  </footer>
</template>

<style scoped>
.footer-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 32px;
}

.footer-link {
  color: #6B7280;
  font-size: 13px;
  text-decoration: none;
  transition: color 0.3s;
}

.footer-link:hover {
  color: #F59E0B;
}

.cert-badge {
  color: #F59E0B;
  font-size: 12px;
  font-weight: 500;
  background: rgba(245,158,11,0.08);
  border: 1px solid rgba(245,158,11,0.15);
  padding: 5px 12px;
  clip-path: polygon(0 0, 100% 0, 100% calc(100% - 6px), calc(100% - 6px) 100%, 0 100%);
  width: fit-content;
}

@media (max-width: 768px) {
  .footer-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .footer-grid {
    grid-template-columns: 1fr;
  }
}
</style>