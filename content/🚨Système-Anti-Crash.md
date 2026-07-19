---
cssclasses: moc-urgence
---

<div style="max-width: 900px; margin: auto; padding: 20px; font-family: 'Inter', sans-serif; background: #0d1117; border-radius: 20px 20px 0 0; border: 1px solid #30363d; border-bottom: none;">
  
  <!-- HEADER MOC -->
  <div style="border-bottom: 2px solid #ff003c; padding-bottom: 15px; margin-bottom: 25px; display: flex; justify-content: space-between; align-items: center;">
    <span style="font-size: 2em; font-weight: 900; color: #ff003c; text-transform: uppercase;">🚨 MOC : ANTI-CRASH</span>
    <a href="/index" style="color: #8b949e; text-decoration: none; border: 1px solid #30363d; padding: 5px 15px; border-radius: 5px; font-weight: bold; background-image: none !important;">⬆️ Retour Cockpit</a>
  </div>

  <!-- HUD STATUT IMMÉDIAT -->
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; margin-bottom: 10px;">
    <div style="background: rgba(255, 0, 60, 0.1); border: 1px solid #ff003c; border-radius: 10px; padding: 15px; text-align: center; animation: pulse-alert 2s infinite;">
      <span style="color: #ff003c; font-weight: 800; font-size: 0.9em; letter-spacing: 1px;">⚠️ SURCHARGE MENTALE DÉTECTÉE</span><br>
      <span style="color: #fff; font-size: 1.5em; font-weight: bold;">[ PROTOCOLE ENGAGÉ ]</span>
    </div>
  </div>
</div>


### 🧭 Graphe de Décision Spatial

_(Les nœuds verts sont cliquables. Ils te téléportent vers l'action.)_



```mermaid
graph TD
    A[🚨 SYMPTÔME ACTUEL ?]
    B[Trop d'onglets mentaux]
    C[Fatigue / Baisse Tolérance]
    D[Optimisation Compulsive]
    
    A --> B
    A --> C
    A --> D
    
    B --> E[[🔒 Vider la RAM]]
    C --> F[[🔋 Rythme Vital]]
    D --> G[[🔇 Isolement]]
    
    %% ROUTAGE DES CLICS (Assure-toi que ces 3 notes existent dans Obsidian)
    click E "/Cloture-Boucles" "Fermer les boucles ouvertes"
    click F "/Protocole-Recuperation" "Retour à l'hygiène de base"
    click G "/Reduction-Bruit" "Couper les stimuli"

    style A fill:#ff003c,stroke:#fff,stroke-width:2px,color:#fff
    style E fill:#00ff41,stroke:#fff,stroke-width:2px,color:#000,cursor:pointer
    style F fill:#00ff41,stroke:#fff,stroke-width:2px,color:#000,cursor:pointer
    style G fill:#00ff41,stroke:#fff,stroke-width:2px,color:#000,cursor:pointer
```

<div style="max-width: 900px; margin: auto; padding: 20px; font-family: 'Inter', sans-serif; background: #0d1117; border-radius: 0 0 20px 20px; border: 1px solid #30363d; border-top: none;">
<!-- GRILLE DE ROUTAGE MANUEL (Redondance) -->
<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin-top: 10px;">
<!-- Carte 1 -->
<a href="/Cloture-Boucles" style="text-decoration: none; background-image: none !important;">
<div class="moc-card" style="border-left: 5px solid #00ff41;">
<span style="font-size: 1.2em; color: #00ff41; font-weight: 800;">🔒 Vider la RAM</span>
<p style="color: #8b949e; margin-top: 8px; font-size: 0.9em;">Fermer 1 chose avant d'en ouvrir 3. Tuer les tâches en cours.</p>
</div>
</a>
<!-- Carte 2 -->
<a href="/Reduction-Bruit" style="text-decoration: none; background-image: none !important;">
<div class="moc-card" style="border-left: 5px solid #58a6ff;">
<span style="font-size: 1.2em; color: #58a6ff; font-weight: 800;">🔇 Isolement</span>
<p style="color: #8b949e; margin-top: 8px; font-size: 0.9em;">Checklist réduction de bruit. Moins de décisions = Plus d'énergie.</p>
</div>
</a>
<!-- Carte 3 -->
<a href="/Protocole-Recuperation" style="text-decoration: none; background-image: none !important;">
<div class="moc-card" style="border-left: 5px solid #b392f0;">
<span style="font-size: 1.2em; color: #b392f0; font-weight: 800;">🔋 Rythme Vital</span>
<p style="color: #8b949e; margin-top: 8px; font-size: 0.9em;">Hygiène de base, limites claires, sommeil et pauses.</p>
</div>
</a>
</div>
</div>

<style>
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