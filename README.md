# 📊 emf-project-2026
**Empirical Methods in Finance — Group Project 2026**

Bienvenue dans ce repository ! Ce guide est fait pour vous si c'est votre **premier projet collaboratif sur GitHub**. Lisez-le attentivement avant de commencer à travailler.

---

## 🧠 C'est quoi GitHub, en deux mots ?

GitHub est un endroit où on stocke du code **en ligne**, et qui garde une **trace de toutes les modifications** faites par chaque membre du groupe. C'est comme Google Docs, mais pour du code — sauf qu'au lieu de modifier en temps réel, chaque personne travaille sur sa propre version locale, puis envoie ses changements.

Les concepts clés à retenir :
- **Repository (repo)** : le dossier du projet, hébergé sur GitHub
- **Clone** : copier le repo sur votre ordinateur pour travailler dessus
- **Commit** : enregistrer une modification avec un message descriptif
- **Push** : envoyer vos commits vers GitHub
- **Pull** : récupérer les dernières modifications faites par vos coéquipiers
- **Branch** : une version parallèle du projet (utile pour travailler sans risquer d'écraser le travail des autres)

---

## 🚀 Mise en place (à faire une seule fois)

### 1. Installer Git
Téléchargez Git sur https://git-scm.com/downloads et installez-le.

### 2. Configurer Git avec votre identité
Ouvrez un terminal (ou Git Bash sur Windows) et tapez :
```bash
git config --global user.name "Votre Prénom Nom"
git config --global user.email "votre@email.com"
```

### 3. Cloner le repository
```bash
git clone https://github.com/yvdri/emf-project-2026.git
```
Cela crée un dossier emf-project-2026 sur votre ordinateur avec tous les fichiers du projet.

### 4. Se déplacer dans le dossier
```bash
cd emf-project-2026
```

---

## 📅 Workflow quotidien (à suivre à chaque session de travail)

> ⚠️ **IMPORTANT : Suivez toujours ces étapes dans l'ordre. Ne les sautez pas.**

### Étape 1 — Récupérez les dernières modifications AVANT de commencer
```bash
git pull origin main
```
Faites ceci **à chaque fois** que vous vous mettez à travailler. Cela évite les conflits.

### Étape 2 — Travaillez sur votre code
Modifiez vos fichiers normalement depuis votre éditeur (VS Code, Jupyter, etc.).

### Étape 3 — Vérifiez ce que vous avez changé
```bash
git status
```
Cette commande vous montre quels fichiers ont été modifiés. Utilisez-la souvent — elle ne fait rien, elle affiche juste l'état.

### Étape 4 — Ajoutez vos fichiers modifiés
Pour ajouter un fichier spécifique :
```bash
git add nom_du_fichier.py
```
Pour ajouter tous les fichiers modifiés :
```bash
git add .
```

### Étape 5 — Enregistrez vos modifications (commit)
```bash
git commit -m "Description courte de ce que vous avez fait"
```
Exemples de bons messages de commit :
- "Ajout de la fonction de régression OLS"
- "Correction du calcul des rendements"
- "Nettoyage des données manquantes dans data_clean.py"

### Étape 6 — Envoyez vos modifications sur GitHub
```bash
git push origin main
```

---

## 🌿 Travailler avec des branches (recommandé pour éviter les conflits)

Plutôt que de travailler tous directement sur main, chaque personne crée sa propre **branche**.

### Créer et basculer sur une nouvelle branche
```bash
git checkout -b prenom/ma-feature
```
Par exemple : git checkout -b rijad/analyse-volatilite

### Vérifier sur quelle branche vous êtes
```bash
git branch
```

### Envoyer votre branche sur GitHub
```bash
git push origin prenom/ma-feature
```

### Fusionner votre branche dans main (via Pull Request)
Ne fusionnez pas directement depuis votre terminal. Allez sur GitHub, cliquez sur "Compare & pull request", et demandez à un coéquipier de relire avant de merger.

---

## 🗂️ Structure suggérée du projet

```
emf-project-2026/
│
├── data/               <- Données brutes (ne pas modifier ces fichiers !)
├── notebooks/          <- Jupyter notebooks d'exploration
├── src/                <- Scripts Python propres et réutilisables
├── results/            <- Graphiques, tableaux de résultats
├── README.md           <- Ce fichier
└── .gitignore          <- Fichiers à ignorer (automatique)
```

---

## ❌ Commandes à éviter (ou à utiliser avec grande précaution)

| Commande | Pourquoi c'est dangereux |
|---|---|
| git push --force | Écrase l'historique sur GitHub, peut supprimer le travail des autres |
| git reset --hard | Supprime définitivement vos modifications locales non sauvegardées |
| git rm -r . | Supprime tous les fichiers du repo |
| Modifier directement sur GitHub ET localement en même temps | Crée des conflits difficiles à résoudre |

---

## ⚡ Résoudre un conflit (si ça arrive)

Un conflit se produit quand deux personnes ont modifié **le même fichier** au même endroit. Git vous le signalera lors d'un pull ou merge.

1. Ouvrez le fichier en conflit — vous verrez des sections comme :
```
<<<<<<< HEAD
votre version du code
=======
version de votre coéquipier
>>>>>>> main
```
2. Choisissez quelle version garder (ou combinez les deux manuellement)
3. Supprimez les marqueurs, puis faites un git add et un git commit

> 💡 Pour éviter les conflits : communiquez avec votre groupe sur qui travaille sur quoi, et faites des git pull fréquents.

---

## 👥 Inviter les membres du groupe

Pour inviter vos coéquipiers au repository privé :
1. Allez dans **Settings** → **Collaborators**
2. Cliquez sur **"Add people"**
3. Entrez leur nom d'utilisateur GitHub ou leur email

---

## 📋 Commandes de référence rapide

```bash
git status          # Voir l'état des fichiers
git pull            # Récupérer les dernières modifications
git add .           # Ajouter tous les fichiers modifiés
git commit -m "msg" # Enregistrer avec un message
git push            # Envoyer sur GitHub
git log --oneline   # Voir l'historique des commits
git branch          # Voir les branches existantes
git checkout -b nom # Créer et basculer sur une nouvelle branche
```

---

## 🆘 En cas de problème

Si vous êtes bloqué :
1. Ne paniquez pas et ne forcez rien
2. Tapez git status pour comprendre l'état du repo
3. Cherchez le message d'erreur sur Google — la communauté Git est très active
4. Demandez à un coéquipier avant de faire une action irréversible

---

*README rédigé pour les membres du projet EMF 2026 — première utilisation de GitHub en groupe.*
