# 🎙️ LecteurVoix — PDF Text-to-Speech

Une application web élégante pour lire des fichiers PDF à voix haute, en français ou en anglais, grâce à l'API Google Cloud Text-to-Speech.

**→ Fonctionne directement depuis GitHub Pages sur iPhone ou n'importe quel navigateur.**

---

## ✨ Fonctionnalités

- 📄 Chargement de PDF par glisser-déposer ou sélection de fichier
- 🔊 Synthèse vocale via Google Cloud TTS (voix Wavenet haute qualité)
- 🇫🇷 Voix françaises et 🇬🇧 anglaises
- ▶️ Lecture, pause, stop et barre de progression
- ⚡ Contrôle de la vitesse de lecture (×0.5 à ×2.0)
- 📑 Navigation page par page et lecture d'une plage de pages
- 💾 Clé API sauvegardée localement dans le navigateur
- 📱 Interface responsive optimisée pour iPhone

---

## 🚀 Déploiement sur GitHub Pages

### 1. Créer le repository

1. Allez sur [github.com/new](https://github.com/new)
2. Nommez-le (ex. : `lecteurvoix` ou `pdf-reader-tts`)
3. Mettez-le en **Public**
4. Cliquez **Create repository**

### 2. Uploader le fichier

**Option A — Interface web (le plus simple) :**
1. Dans votre nouveau repository, cliquez **Add file → Upload files**
2. Glissez le fichier `index.html`
3. Cliquez **Commit changes**

**Option B — Git en ligne de commande :**
```bash
git clone https://github.com/VOTRE_NOM/VOTRE_REPO.git
cd VOTRE_REPO
cp /chemin/vers/index.html .
git add index.html
git commit -m "Ajout de LecteurVoix"
git push
```

### 3. Activer GitHub Pages

1. Dans votre repository → **Settings** → **Pages** (menu gauche)
2. Source : **Deploy from a branch**
3. Branch : **main** / **root**
4. Cliquez **Save**
5. Après ~1 minute, votre app est disponible à :  
   `https://VOTRE_NOM.github.io/VOTRE_REPO/`

### 4. Ajouter sur l'écran d'accueil iPhone

1. Ouvrez l'URL dans **Safari** sur votre iPhone
2. Appuyez sur le bouton Partager (□↑)
3. **Ajouter à l'écran d'accueil**
4. L'app se comporte comme une app native !

---

## 🔑 Configuration de la clé API Google Cloud TTS

### Obtenir une clé API

1. Allez sur [console.cloud.google.com](https://console.cloud.google.com)
2. Créez un projet (ou sélectionnez-en un existant)
3. Activez l'API : **APIs & Services → Library → Cloud Text-to-Speech API**
4. **APIs & Services → Credentials → Create Credentials → API Key**
5. Copiez la clé générée

### Sécuriser la clé (recommandé)

Dans la console Google Cloud, restreignez la clé :
- **Application restrictions** : HTTP referrers
- Ajoutez `https://VOTRE_NOM.github.io/*`
- **API restrictions** : Cloud Text-to-Speech API

### Dans l'application

1. Ouvrez l'app dans votre navigateur
2. Collez la clé dans le champ **Clé API**
3. Cliquez **✓ Sauver** — elle est stockée localement dans votre navigateur

> ⚠️ La clé est stockée dans `localStorage` de votre navigateur uniquement. Elle n'est jamais envoyée nulle part sauf aux serveurs Google TTS.

---

## 💰 Tarification Google Cloud TTS

- **Voix Standard** : 1M caractères gratuits/mois, puis $4/1M
- **Voix WaveNet** : 1M caractères gratuits/mois, puis $16/1M
- Un PDF de 10 pages ≈ 5 000–10 000 caractères → très économique

---

## 🛠️ Technologies

- HTML/CSS/JS pur — aucune dépendance NPM
- [PDF.js](https://mozilla.github.io/pdf.js/) pour l'extraction de texte
- [Google Cloud Text-to-Speech API](https://cloud.google.com/text-to-speech)
- Web Audio API pour la lecture audio

---

## 📝 Licence

MIT — libre d'utilisation et de modification.
