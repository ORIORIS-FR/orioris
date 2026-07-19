---
created_at: 2026-07-18T20:07
updated_at: 2026-07-18T20:16
cssclasses:
---
![[Xurta_photo.jpg]]

<div style="max-width: 900px; margin: auto; padding: 20px; font-family: 'Inter', sans-serif; background: #0d1117; border-radius: 20px; border: 1px solid #30363d; box-shadow: 0 0 30px rgba(0,0,0,0.5);">
  <!-- HEADER MOC -->
  <div style="border-bottom: 2px solid #b392f0; padding-bottom: 15px; margin-bottom: 25px; display: flex; justify-content: space-between; align-items: center;">
    <span style="font-size: 2em; font-weight: 900; color: #b392f0; text-transform: uppercase;">💊 MOC : Neuro-Chimie</span>
    <a href="/index" style="color: #8b949e; text-decoration: none; border: 1px solid #30363d; padding: 5px 15px; border-radius: 5px; font-weight: bold;">⬆️ Retour Cockpit</a>
  </div>
  <!-- HUD STATUT IMMÉDIAT (Monitoring) -->
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; margin-bottom: 30px;">
    <!-- Jauge d'état -->
    <div style="background: rgba(179, 146, 240, 0.1); border: 1px solid #b392f0; border-radius: 10px; padding: 15px; text-align: center;">
      <span style="color: #b392f0; font-weight: 800; font-size: 0.9em; letter-spacing: 1px;">⚡ ÉQUILIBRE DOPAMINE</span><br>
      <span style="color: #fff; font-size: 1.5em; font-weight: bold;">[ CALIBRAGE EN COURS ]</span>
    </div>
    <!-- Alerte Logistique (Taxe TDAH) -->
    <div style="background: rgba(255, 0, 60, 0.1); border: 1px solid #ff003c; border-radius: 10px; padding: 15px; text-align: center; animation: pulse-alert 2s infinite;">
      <span style="color: #ff003c; font-weight: 800; font-size: 0.9em; letter-spacing: 1px;">⚠️ RENOUVELLEMENT ORDONNANCE</span><br>
      <span style="color: #fff; font-size: 1.5em; font-weight: bold;">[ J - 5 ]</span>
    </div>
  </div>
  <!-- GRILLE DE ROUTAGE (Briques Atomiques de Niveau 3) -->
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px;">
        <!-- Carte 1 : La Science -->
    <a href="/Pharmacocinetique" style="text-decoration: none;">
      <div class="moc-card" style="border-left: 5px solid #b392f0;">
        <span style="font-size: 1.2em; color: #b392f0; font-weight: 800;">🧪 La Molécule</span>
        <p style="color: #8b949e; margin-top: 8px; font-size: 0.9em;">Dosage cible, demi-vie, mécanisme sur les récepteurs.</p>
      </div>
    </a>
    <!-- Carte 2 : Le Tracking -->
    <a href="/Journal-Effets" style="text-decoration: none;">
      <div class="moc-card" style="border-left: 5px solid #58a6ff;">
        <span style="font-size: 1.2em; color: #58a6ff; font-weight: 800;">📈 Tracking & Crash</span>
        <p style="color: #8b949e; margin-top: 8px; font-size: 0.9em;">Logs quotidiens. Heure de prise vs Heure du crash de rebond.</p>
      </div>
    </a>
    <!-- Carte 3 : Les Dangers -->
    <a href="/Interactions-Rouges" style="text-decoration: none;">
      <div class="moc-card" style="border-left: 5px solid #ff003c;">
        <span style="font-size: 1.2em; color: #ff003c; font-weight: 800;">🚫 Liste Noire (Interactions)</span>
        <p style="color: #8b949e; margin-top: 8px; font-size: 0.9em;">Vitamine C, Caféine, et acides bloquant l'absorption.</p>
      </div>
    </a>
    <!-- Carte 4 : L'Administration -->
    <a href="/Logistique-Medicale" style="text-decoration: none;">
      <div class="moc-card" style="border-left: 5px solid #00ff41;">
        <span style="font-size: 1.2em; color: #00ff41; font-weight: 800;">📅 Protocole Logistique</span>
        <p style="color: #8b949e; margin-top: 8px; font-size: 0.9em;">Contacts pharmacie, agenda psychiatre, protocole de sécurité.</p>
      </div>
    </a>
  </div>
</div>
<style>
  /* ANIMATIONS ET EFFETS DE SURVOL INJECTÉS DIRECTEMENT */
  @keyframes pulse-alert { 
    0%, 100% { box-shadow: 0 0 5px rgba(255, 0, 60, 0.2); } 
    50% { box-shadow: 0 0 20px rgba(255, 0, 60, 0.6); } 
  }
  .moc-card {
    background: rgba(255,255,255,0.02); 
    padding: 20px; 
    border-radius: 8px; 
    border-top: 1px solid #30363d; 
    border-right: 1px solid #30363d; 
    border-bottom: 1px solid #30363d; 
    height: 100%; 
    transition: all 0.2s ease-in-out;
  }
  a:hover .moc-card { 
    filter: brightness(1.3); 
    transform: translateY(-3px);
    background: rgba(255,255,255,0.05);
  }
</style>