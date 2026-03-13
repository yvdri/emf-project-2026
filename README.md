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
- **Branch** : une version parallèle du projet (expliqué en détail plus bas !)

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

## 🌿 Les branches — explication complète pour débutants

> ⚠️ C'est la partie la plus importante pour travailler en groupe sans se marcher dessus.

### D'abord : c'est quoi une branche ?

Une branche **n'est pas un nouveau fichier** et **n'est pas un nouveau dossier**. C'est une **version parallèle de tout le projet** qui existe uniquement dans Git.

Imaginez que le projet est un document Word. Sans branches, tout le monde ouvre et modifie le même document en même temps — résultat : le chaos. Avec des branches, chaque personne travaille sur **sa propre copie**, et quand c'est prêt, on fusionne tout ensemble proprement.

La branche principale s'appelle `main`. C'est la version "officielle" du projet.  
**Règle d'or : on ne travaille jamais directement sur `main`.**

---

### Exemple concret avec 4 personnes

Disons que votre groupe s'appelle Alice, Bob, Charlie et Rijad. Chacun a une tâche différente :

| Personne | Tâche |
|---|---|
| Rijad | Nettoyage des données |
| Alice | Régression OLS |
| Bob | Visualisation des résultats |
| Charlie | Rédaction du rapport |

Chacun crée **sa propre branche** et travaille dedans sans gêner les autres.

---

### Comment utiliser les branches — pas à pas

#### 1. Avant de commencer à travailler, mettez-vous à jour
```bash
git pull origin main
```

#### 2. Créez votre branche personnelle et basculez dessus
```bash
git checkout -b rijad/nettoyage-donnees
```
> Cette commande fait deux choses à la fois : elle **crée** la branche ET vous **place dessus** automatiquement.
> Le nom de la branche peut être ce que vous voulez. Convention recommandée : `prenom/description-courte`

#### 3. Vérifiez que vous êtes bien sur votre branche
```bash
git branch
```
Vous verrez une liste de branches. Celle avec une `*` devant est celle sur laquelle vous êtes actuellement :
```
  main
* rijad/nettoyage-donnees
```

#### 4. Travaillez normalement sur vos fichiers
Ouvrez VS Code, modifiez vos scripts Python, vos notebooks... Tout ce que vous faites ici **ne touche pas à `main`**. Vous êtes en sécurité.

#### 5. Sauvegardez votre travail (add + commit) comme d'habitude
```bash
git add .
git commit -m "Nettoyage des valeurs manquantes dans les prix"
```

#### 6. Envoyez votre branche sur GitHub
```bash
git push origin rijad/nettoyage-donnees
```

#### 7. Créez une Pull Request sur GitHub pour fusionner dans main

C'est l'étape finale : vous proposez d'intégrer votre travail dans la version officielle.

1. Allez sur https://github.com/yvdri/emf-project-2026
2. GitHub va afficher une bannière jaune : **"Compare & pull request"** — cliquez dessus
3. Ajoutez un titre et une description de ce que vous avez fait
4. Cliquez sur **"Create pull request"**
5. Un coéquipier relit votre travail et clique sur **"Merge pull request"**
6. Votre travail est maintenant dans `main` ! 🎉

#### 8. Après la fusion, revenez sur main et mettez-vous à jour
```bash
git checkout main
git pull origin main
```

---

### Résumé visuel du flux de travail avec branches

```
main ──────────────────────────────────────────► (version officielle)
         │                              ▲
         │ git checkout -b              │ Pull Request + Merge
         ▼                              │
rijad/nettoyage ── commit ── commit ── push
```

---

### Les erreurs fréquentes à éviter avec les branches

| Erreur | Conséquence | Solution |
|---|---|---|
| Oublier de créer une branche et travailler sur `main` | Risque d'écraser le travail des autres | Toujours vérifier avec `git branch` avant de commencer |
| Oublier de faire `git pull` avant de créer sa branche | Votre branche part d'une version ancienne | Toujours `git pull origin main` en premier |
| Pusher directement sur `main` sans Pull Request | Pas de relecture, risque de bugs | Toujours passer par une Pull Request |

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
| `git push --force` | Écrase l'historique sur GitHub, peut supprimer le travail des autres |
| `git reset --hard` | Supprime définitivement vos modifications locales non sauvegardées |
| `git rm -r .` | Supprime tous les fichiers du repo |
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
3. Supprimez les marqueurs, puis faites un `git add` et un `git commit`

> 💡 Pour éviter les conflits : communiquez avec votre groupe sur qui travaille sur quoi, et faites des `git pull` fréquents.

---

## 👥 Inviter les membres du groupe

Pour inviter vos coéquipiers au repository privé :
1. Allez dans **Settings** → **Collaborators**
2. Cliquez sur **"Add people"**
3. Entrez leur nom d'utilisateur GitHub ou leur email

---

## 📋 Commandes de référence rapide

```bash
git status                        # Voir l'état des fichiers
git pull origin main              # Récupérer les dernières modifications
git checkout -b prenom/ma-tache   # Créer et basculer sur une nouvelle branche
git branch                        # Vérifier sur quelle branche on est
git add .                         # Ajouter tous les fichiers modifiés
git commit -m "message"           # Enregistrer avec un message
git push origin prenom/ma-tache   # Envoyer sa branche sur GitHub
git checkout main                 # Revenir sur main
git log --oneline                 # Voir l'historique des commits
```

---

## 🆘 En cas de problème

Si vous êtes bloqué :
1. **Ne paniquez pas et ne forcez rien**
2. Tapez `git status` pour comprendre l'état du repo
3. Tapez `git branch` pour savoir sur quelle branche vous êtes
4. Cherchez le message d'erreur sur Google — la communauté Git est très active
5. Demandez à un coéquipier avant de faire une action irréversible

---

*README rédigé pour les membres du projet EMF 2026 — première utilisation de GitHub en groupe.*
