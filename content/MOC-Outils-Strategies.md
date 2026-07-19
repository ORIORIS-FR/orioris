---
cssclasses: moc-armurerie
---
---
cssclasses: moc-armurerie
---

<div style="max-width: 900px; margin: auto; padding: 20px; font-family: 'Inter', sans-serif; background: linear-gradient(145deg, #0d1117, #161b22); border-radius: 20px 20px 0 0; border: 1px solid #30363d; border-bottom: none; box-shadow: 0 10px 30px rgba(0,0,0,0.8);">
<!-- HEADER MOC -->
<div style="border-bottom: 2px solid #f2ce5a; padding-bottom: 15px; margin-bottom: 25px; display: flex; justify-content: space-between; align-items: center;">
<span style="font-size: 2em; font-weight: 900; color: #f2ce5a; text-transform: uppercase;"> Concepts 💡 Idées 💡 Produits 
🧰 Caisse à Outils 🛠️  
(Neuro-Hardware)</span>
<a href="/index" style="color: #8b949e; text-decoration: none; border: 1px solid #30363d; padding: 5px 15px; border-radius: 5px; font-weight: bold; background: #0d1117; background-image: none !important;">⬆️ Retour Cockpit</a>
</div>
<!-- HUD SENSORIEL -->
<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; margin-bottom: 10px;">
<div style="background: rgba(242, 206, 90, 0.05); border: 1px solid #f2ce5a; border-radius: 10px; padding: 15px; text-align: center; box-shadow: inset 0 0 15px rgba(242, 206, 90, 0.1);">
<span style="color: #f2ce5a; font-weight: 800; font-size: 0.9em; letter-spacing: 1px;">📡 CHARGE SENSORIELLE</span><br>
<span style="color: #fff; font-size: 1.5em; font-weight: bold;">[ MESURE EN COURS ]</span>
</div>
</div>
</div>

### 🧭 Interface de Déploiement Matériel (VSL Interactive)

*(Graphe de routage : Clique sur les modules pour accéder à l'équipement).*

```mermaid

graph TD
    A{"⚙️ SÉLECTION<br>DE L'ÉQUIPEMENT"}
    
    A -->|"Régulation Temporelle"| B(("⏳ ANCRAGE<br>CINÉTIQUE"))
    A -->|"Isolation Acoustique"| C(("🎧 BOUCLIER<br>NEURO-HAPTIQUE"))
    A -->|"Récupération Physique"| D(("🏠 DOMOTIQUE<br>PRÉDICTIVE"))
    
    %% ROUTAGE DES CLICS 
    click B "/outils/Outils-Ancrage-Cinetique" "Minuteurs à gravité et objets tangibles"
    click C "/outils/Outils-Bouclier-Sensoriel" "IEM EEG & Infrabasses"
    click D "/outils/Outils-Domotique-Predictive" "IoT & Récupération"

    %% STYLISATION SOMBRE TEXTURÉE (Orioris Standard)
    style A fill:#1a1a2e,stroke:#f2ce5a,stroke-width:3px,color:#f2ce5a
    style B fill:#161b22,stroke:#f2ce5a,stroke-width:2px,color:#fff,cursor:pointer
    style C fill:#161b22,stroke:#f2ce5a,stroke-width:2px,color:#fff,cursor:pointer
    style D fill:#161b22,stroke:#f2ce5a,stroke-width:2px,color:#fff,cursor:pointer
    
    linkStyle 0,1,2 stroke:#f2ce5a,stroke-width:2px,color:#fff
    
```