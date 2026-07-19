---
cssclasses: moc-armurerie
---

<style>
    /* ENCAPSULATION STRICTE POUR PROTÉGER QUARTZ */
    #orioris-tinder-app {
        --bg: #1a1a2e; /* Fond Orioris */
        --card-bg: #161b22; /* Cartes Orioris */
        --text: #ffffff;
        --accent: #f2ce5a; /* Jaune Orioris */
        --green: #00ff41; /* Vert Matrix */
        --red: #ff3333;
        --blue: #58a6ff;
        
        font-family: 'Inter', system-ui, sans-serif;
        background-color: var(--bg);
        color: var(--text);
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        min-height: 80vh; /* Adapté pour Quartz au lieu du 100vh absolu */
        width: 100%;
        border-radius: 12px;
        border: 1px solid #30363d;
        padding: 20px;
        box-sizing: border-box;
    }

    #orioris-tinder-app #game-container {
        text-align: center;
        width: 100%;
        max-width: 500px;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    #orioris-tinder-app .progress-container {
        width: 100%;
        background-color: #30363d;
        border-radius: 10px;
        margin-bottom: 20px;
        height: 10px;
        overflow: hidden;
    }

    #orioris-tinder-app .progress-bar {
        height: 100%;
        background-color: var(--accent);
        width: 0%;
        transition: width 0.3s;
    }

    #orioris-tinder-app .card {
        background-color: var(--card-bg);
        padding: 40px 20px;
        border-radius: 20px;
        box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        font-size: 1.5rem; 
        font-weight: bold;
        min-height: 180px;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-bottom: 30px;
        border: 2px solid #30363d;
        transition: transform 0.2s, border-color 0.2s;
        cursor: default;
        user-select: none;
        box-sizing: border-box;
        position: relative;
    }
    
    #orioris-tinder-app .new-badge {
        position: absolute;
        top: -10px;
        right: -10px;
        background: var(--accent);
        color: #000;
        font-size: 0.7rem;
        padding: 5px 10px;
        border-radius: 10px;
        transform: rotate(5deg);
        font-weight: 900;
    }

    #orioris-tinder-app .controls {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 15px;
        width: 100%;
    }

    #orioris-tinder-app .btn {
        border: none;
        padding: 15px;
        border-radius: 12px;
        font-size: 1.2rem;
        font-weight: bold;
        cursor: pointer;
        transition: transform 0.1s;
        color: white;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    #orioris-tinder-app .btn:active { transform: scale(0.95); }
    #orioris-tinder-app .btn-no { background-color: var(--red); color: white;}
    #orioris-tinder-app .btn-dev { background-color: var(--blue); color: black; }
    #orioris-tinder-app .btn-yes { background-color: var(--green); color: black; }
    
    #orioris-tinder-app .btn-stop {
        margin-top: 25px;
        background: transparent;
        border: 1px solid #555;
        color: #aaa;
        padding: 10px 20px;
        border-radius: 8px;
        cursor: pointer;
        font-size: 0.9rem;
    }
    #orioris-tinder-app .btn-stop:hover { border-color: var(--accent); color: var(--accent); }
    
    #orioris-tinder-app .key-hint { font-size: 0.7rem; opacity: 0.7; margin-top: 5px; font-weight: normal; }

    #orioris-tinder-app #results-container {
        display: none;
        width: 100%;
        max-width: 800px;
        max-height: 70vh;
        overflow-y: auto;
        background: var(--card-bg);
        padding: 30px;
        border-radius: 15px;
        border: 1px solid #30363d;
    }
    
    #orioris-tinder-app .result-group { margin-bottom: 30px; text-align: left; }
    #orioris-tinder-app .result-group h3 { border-bottom: 2px solid #30363d; padding-bottom: 10px; color: var(--accent); }
    #orioris-tinder-app .tag-cloud { display: flex; flex-wrap: wrap; gap: 10px; }
    #orioris-tinder-app .tag { padding: 5px 12px; border-radius: 15px; font-size: 0.9rem; background: #0d1117; }
    #orioris-tinder-app .tag.yes { border: 1px solid var(--green); color: var(--green); }
    #orioris-tinder-app .tag.dev { border: 1px solid var(--blue); color: var(--blue); }

    #orioris-tinder-app .btn-copy {
        background-color: var(--accent);
        color: #000;
        padding: 15px 30px;
        font-size: 1.2rem;
        font-weight: 900;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        margin-top: 20px;
        width: 100%;
    }

    #orioris-tinder-app .btn-reset {
        background: transparent;
        color: var(--red);
        border: 1px solid var(--red);
        padding: 10px;
        margin-top: 30px;
        cursor: pointer;
        font-size: 0.8rem;
        border-radius: 5px;
    }
</style>

<div id="orioris-tinder-app">
    <div id="game-container">
        <h2 style="margin-top:0; color:#888; font-size:1rem; text-transform: uppercase; letter-spacing: 2px;">⚡ TRI SOFT SKILLS (Auto-Save)</h2>
        
        <div class="progress-container">
            <div class="progress-bar" id="progress"></div>
        </div>
        
        <div class="card" id="tinder-card">
            Chargement...
        </div>

        <div class="controls">
            <button class="btn btn-no" onclick="vote('no')">❌ NON <span class="key-hint">←</span></button>
            <button class="btn btn-dev" onclick="vote('dev')">🚀 À BOSSER <span class="key-hint">↑</span></button>
            <button class="btn btn-yes" onclick="vote('yes')">✅ OUI <span class="key-hint">→</span></button>
        </div>
        
        <p style="margin-top:10px; font-size:0.8rem; color:#8b949e; font-family: 'JetBrains Mono', monospace;">
            <span id="counter">0</span> / 235
        </p>

        <button class="btn-stop" onclick="finishGame()">🏁 Voir mes résultats (Pause)</button>
        <div id="save-msg" style="font-size:0.7rem; color:var(--green); opacity:0; transition:opacity 1s; margin-top:5px;">Progression sauvegardée</div>
    </div>

    <div id="results-container">
        <h1 style="text-align:center; color: var(--accent);">📊 Bilan Opérationnel</h1>
        <p style="text-align:center; color:#8b949e;" id="result-subtitle"></p>

        <button class="btn-copy" onclick="copyToClipboard()">📋 Exporter vers Obsidian</button>
        <p id="copy-feedback" style="text-align:center; color:var(--green); opacity:0; font-weight: bold; margin-top: 10px;">Données copiées dans le presse-papier !</p>

        <div class="result-group">
            <h3>🚀 MODULES À DÉVELOPPER</h3>
            <div class="tag-cloud" id="list-dev"></div>
        </div>

        <div class="result-group">
            <h3>✅ FORCES VALIDÉES</h3>
            <div class="tag-cloud" id="list-yes"></div>
        </div>
        
        <div style="text-align:center; margin-top: 40px; padding-top: 20px; border-top: 1px solid #30363d;">
             <button class="btn-stop" onclick="location.reload()" style="border-color:var(--green); color:var(--green);">▶️ Reprendre le tri</button>
             <br>
             <button class="btn-reset" onclick="resetData()">🗑️ Purger la mémoire</button>
        </div>
    </div>
</div>

<script>
    // --- DONNÉES SOURCES ---
    const allTraits = [
        "Capable de reconnaître mes erreurs", "Capable de respecter les délais", "Capable d'aller au bout des projets", "Calme",
        "Capable d'exprimer ses sentiments de façon directe", "Capable de relations durables", "Capable d'entrer dans le coeur du sujet",
        "Audacieux", "Capable d'une attitude critique", "A la recherche de défis", "Chaleureux", "Clair dans sa pensée",
        "Capable de travailler sous pression", "Rusé", "Conformiste", "Passif", "Méticuleux", "Soucieux de finaliser",
        "Porté vers l'action", "Actif", "Adapté", "Agressif", "Anxieux", "Capable de hiérarchiser mes priorités",
        "Attaché à mes propres buts", "Capable de planifier efficacement", "Soigneux", "Capable de bien travailler dans un environnement sécurité",
        "Capable de m'exprimer librement", "Capable de profiter au mieux de mon temps", "Gai", "Charismatique", "Circonspect",
        "Capable de réfléchir avant d'agir", "Communicatif", "Capable de retomber sur mes pieds", "Compatissant", "Compétent",
        "Compétitif", "Concentré", "Concerné par les autres", "Concis", "Confiant", "Convenable", "Aventurier",
        "Conscient", "Concerné par le développement humain", "Charmant", "Curieux de moi-même", "Aspirant à mieux",
        "Conventionnel", "Logique", "Amoureux", "Loyal", "Mâture", "Méthodique", "Original", "Convivial", "Franc",
        "Patient", "Extraverti", "Perceptif", "Me dépasse sous la pression", "Persévérant", "Persistant", "Personnel",
        "Persuasif", "Bon joueur", "Equilibré", "Positif", "Pratique", "Tourné vers l'action", "Productif", "Professionnel",
        "Progressif", "Prend facilement des initiatives", "Aime apprendre", "Digne de confiance", "Prudent", "Exact",
        "Réservé", "Rebondir facilement", "Plein de ressources", "Responsable", "Emotif", "Tranquille", "Concerné par les résultats",
        "Prendre des risques", "Assuré", "Bien dans sa peau", "Sûr de moi", "Lucide", "Contrôle de soi", "Auto-discipliné",
        "Capable de me motiver", "Autonome", "Doué du sens de l'humour", "Sensible", "Attentif", "Grave", "Dévoué",
        "Perspicace", "Sincère", "Sociable", "Avoir le sens social", "Spontané", "Equitable", "Anticipateur", "Convainquant",
        "Volontaire", "Sympathique", "Plein de tact", "Ingénu", "Crédible", "Hésitant", "Curieux", "Large d'esprit",
        "Pragmatique", "Décidé", "Dévoué à mon organisation", "Attaché à mes idées", "Egocentriste", "Dépendant",
        "Minutieux", "Déterminé", "Agile", "Diligent", "Diplomate", "Direct", "Discret", "Réfléchi", "Dynamique",
        "Passionné", "Rapidement motivé", "Insouciant", "Econome", "Trouve rapidement des solutions", "Efficace",
        "Emotionnellement stable", "Energique", "Entreprenant", "Enthousiaste", "Motivant", "Ponctuel", "Excité par les défis",
        "Expressif", "Factuel", "Visionnaire", "Adroit dans le raisonnement", "Ferme", "Souple", "Puissant", "Prévoyant",
        "Amical", "Généreux", "Naturel", "Bon équilibre psycho", "D'un bon jugement", "Impartial", "Capable d'écoute",
        "Doté de bon sens", "Se sent bien en groupe", "Laborieux", "Bon coéquipier", "Prévenant", "Honnête", "Humanitaire",
        "Idéaliste", "Imaginatif", "Indépendant", "Individualiste", "Ingénieux", "Initiateur", "Innovateur", "Introspectif",
        "Intègre", "Intellectuel", "En harmonie avec ses sentiments", "Introverti", "Intuitif", "Inventif",
        "Curieux du monde extérieur", "Concerné", "Equipier idéal", "Tenace", "Consciencieux", "Rationnel", "Concret",
        "Raisonnable", "Méditatif", "Soucieux des autres", "Tolérant", "Indifférent à la routine", "Solide mentalement",
        "Plein de confiance", "Digne de foi", "Sans prétention", "Peu émotif", "Compréhensif", "Peu ambitieux",
        "Sans égoïsme", "Aventureux", "S'exprime avec facilité", "Versatile", "Accueillant", "Soigné", "Avide de savoir",
        "Sage", "Endurant les missions de longue durée", "Spirituel", "Alerte", "Ambitieux", "Analytique", "Sûr de soi",
        "Astucieux", "Attentif au détail", "Conservateur", "Calme après la tempête", "Coopératif", "Courageux", "Créatif",
        "A la recherche de responsabilités"
    ];

    // --- GESTION ÉTAT (LOCALSTORAGE) ---
    let state = {
        queue: [], 
        done: { yes: [], no: [], dev: [] },
        total: allTraits.length
    };

    const cardEl = document.getElementById('tinder-card');
    const progressEl = document.getElementById('progress');
    const counterEl = document.getElementById('counter');

    function loadState() {
        const saved = localStorage.getItem('orioris_softskills_v1');
        if (saved) {
            state = JSON.parse(saved);
        } else {
            state.queue = shuffleArray([...allTraits]);
        }
    }

    function saveState() {
        localStorage.setItem('orioris_softskills_v1', JSON.stringify(state));
        const msg = document.getElementById('save-msg');
        msg.style.opacity = 1;
        setTimeout(() => msg.style.opacity = 0, 1000);
    }

    function shuffleArray(array) {
        for (let i = array.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [array[i], array[j]] = [array[j], array[i]];
        }
        return array;
    }

    function init() {
        loadState();
        renderCard();
        updateProgress();
        
        // Clavier sécurisé pour éviter d'activer le scroll natif du navigateur
        document.addEventListener('keydown', (e) => {
            if(document.getElementById('game-container').style.display === 'none') return;
            if (e.key === 'ArrowLeft') { e.preventDefault(); vote('no'); }
            if (e.key === 'ArrowRight') { e.preventDefault(); vote('yes'); }
            if (e.key === 'ArrowUp') { e.preventDefault(); vote('dev'); }
        });
    }

    function renderCard() {
        if (state.queue.length === 0) {
            finishGame();
            return;
        }
        const currentTrait = state.queue[0];
        cardEl.className = 'card';
        void cardEl.offsetWidth; 
        cardEl.innerHTML = currentTrait + (isNewSession() ? `<div class="new-badge">Suite...</div>` : "");
    }

    function isNewSession() { return false; }

    function vote(choice) {
        if (state.queue.length === 0) return;

        const trait = state.queue.shift(); 
        state.done[choice].push(trait);    
        saveState(); 

        // Rendu Visuel
        if(choice === 'no') { cardEl.style.borderColor = 'var(--red)'; }
        else if(choice === 'yes') { cardEl.style.borderColor = 'var(--green)'; }
        else { cardEl.style.borderColor = 'var(--blue)'; }

        setTimeout(() => {
            renderCard();
            updateProgress();
        }, 150);
    }

    function updateProgress() {
        const doneCount = state.done.yes.length + state.done.no.length + state.done.dev.length;
        const pct = Math.round((doneCount / state.total) * 100);
        progressEl.style.width = pct + '%';
        counterEl.innerText = `${doneCount} / ${state.total}`;
    }

    function finishGame() {
        document.getElementById('game-container').style.display = 'none';
        document.getElementById('results-container').style.display = 'block';

        const doneCount = state.done.yes.length + state.done.no.length + state.done.dev.length;
        document.getElementById('result-subtitle').innerText = `${doneCount} éléments analysés sur ${state.total}`;

        displayTags('list-dev', state.done.dev, 'dev');
        displayTags('list-yes', state.done.yes, 'yes');
    }

    function displayTags(id, arr, type) {
        const el = document.getElementById(id);
        el.innerHTML = arr.length ? "" : "<em>Aucune donnée</em>";
        arr.forEach(t => {
            el.innerHTML += `<span class="tag ${type}">${t}</span>`;
        });
    }

    function copyToClipboard() {
        let md = "---\ntags: [bilan, soft-skills]\n---\n# 🧠 Bilan Soft Skills\n\n";
        md += `> [!info] Progression du Tri\n> Avancement : ${document.getElementById('counter').innerText}\n\n`;
        
        md += "## 🚀 Modules à Développer\n";
        state.done.dev.forEach(t => md += `- [ ] ${t}\n`);
        
        md += "\n## ✅ Forces Validées\n";
        state.done.yes.forEach(t => md += `- ${t}\n`);

        navigator.clipboard.writeText(md).then(() => {
            document.getElementById('copy-feedback').style.opacity = 1;
            setTimeout(() => document.getElementById('copy-feedback').style.opacity = 0, 2000);
        });
    }

    function resetData() {
        if(confirm("ALERTE : Purge de la mémoire enclenchée. Confirmer la suppression ?")) {
            localStorage.removeItem('orioris_softskills_v1');
            location.reload();
        }
    }

    // Lancement du module
    setTimeout(init, 100); // Léger délai pour s'assurer que le DOM de Quartz est prêt
</script>