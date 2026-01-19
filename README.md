# PDF Presenter 📽️

Un site web élégant pour héberger et présenter vos PDFs en mode présentation (16:9), protégé par mot de passe.

## 🚀 Déploiement sur GitHub Pages

### Étape 1 : Créer le repository

1. Créez un nouveau repository sur GitHub
2. Uploadez tous les fichiers de ce dossier dans le repository :
   - `index.html`
   - `pdfs.json`
   - Créez un dossier `pdfs/` pour vos fichiers PDF

### Étape 2 : Activer GitHub Pages

1. Allez dans **Settings** > **Pages**
2. Dans "Source", sélectionnez **Deploy from a branch**
3. Choisissez la branche `main` et le dossier `/ (root)`
4. Cliquez sur **Save**
5. Attendez quelques minutes, votre site sera accessible à `https://votre-username.github.io/nom-du-repo/`

## 📁 Structure du projet

```
votre-repo/
├── index.html          # Page principale
├── pdfs.json           # Liste des PDFs à afficher
├── pdfs/               # Dossier contenant vos PDFs
│   ├── presentation1.pdf
│   ├── presentation2.pdf
│   └── ...
└── README.md
```

## ➕ Ajouter un nouveau PDF

### 1. Uploadez votre PDF

Ajoutez votre fichier PDF dans le dossier `pdfs/` de votre repository GitHub.

### 2. Modifiez pdfs.json

Éditez le fichier `pdfs.json` pour ajouter votre nouveau PDF :

```json
[
    {
        "name": "Ma Nouvelle Présentation",
        "file": "pdfs/ma-presentation.pdf",
        "date": "2024-03-20"
    },
    {
        "name": "Autre Présentation",
        "file": "pdfs/autre.pdf",
        "date": "2024-03-15"
    }
]
```

### 3. Commit et Push

Commitez vos modifications et poussez-les sur GitHub. Le site se mettra à jour automatiquement.

## 🔐 Mot de passe

Le mot de passe par défaut est : `123456`

Pour le modifier, éditez la ligne suivante dans `index.html` :

```javascript
const PASSWORD = '123456';
```

⚠️ **Note de sécurité** : Ce système de mot de passe est basique et côté client. Il n'offre pas une sécurité robuste. Ne l'utilisez pas pour des contenus hautement confidentiels.

## 🎮 Utilisation

### Navigation en mode présentation

- **Flèche droite** ou **Espace** : Page suivante
- **Flèche gauche** : Page précédente
- **Échap** : Fermer la présentation
- Vous pouvez aussi cliquer sur les flèches ou les points de navigation

### Prévisualisation temporaire

Vous pouvez glisser-déposer un PDF depuis votre ordinateur pour le prévisualiser temporairement (non sauvegardé sur GitHub).

## ✨ Fonctionnalités

- 🔒 Protection par mot de passe
- 📱 Design responsive (fonctionne sur mobile)
- 🎨 Interface moderne et élégante
- 📄 Miniatures automatiques des PDFs
- 🖥️ Mode présentation plein écran (16:9)
- ⌨️ Navigation au clavier
- 🌙 Thème sombre

## 🛠️ Personnalisation

### Changer les couleurs

Les variables CSS sont définies au début du fichier `index.html` :

```css
:root {
    --accent: #6366f1;        /* Couleur principale */
    --bg-primary: #0a0a0f;    /* Arrière-plan */
    --text-primary: #f0f0f5;  /* Couleur du texte */
    /* ... */
}
```

## 📝 Licence

Libre d'utilisation pour un usage personnel.
