# 🧠 Cours rapide de Git

## 🔹 Git, c’est quoi ?
Git est un **système de contrôle de version distribué** qui permet de suivre les modifications d’un projet, collaborer avec d’autres et revenir à des versions antérieures facilement. Chaque développeur possède une **copie complète de l’historique** sur sa machine. :contentReference[oaicite:0]{index=0}

---

## 🔹 Version control ?
Le **contrôle de version** (Version Control System – VCS) est une technologie qui enregistre l’historique des modifications d’un code/projet. Elle permet de savoir *qui a fait quoi*, *quand*, et de revenir à une version précédente si besoin. :contentReference[oaicite:1]{index=1}

---

## 🔹 Centralisé / Distribué ?
### 📌 Centralisé
- Un **serveur unique** stocke tout l’historique.
- Les développeurs récupèrent et envoient les modifications via ce serveur.

**Avantages :**
- Simple à comprendre
- Historique *centralisé*

**Inconvénients :**
- Si le serveur tombe, tout s’arrête
- On ne peut pas travailler hors ligne facilement

### 📌 Distribué (comme Git)
- Chaque dev a **l’historique complet localement**.
- On peut faire des actions sans serveur puis *push/pull* plus tard.

**Avantages :**
- Travaille hors ligne
- Très rapide
- Plus de sécurité des données

**Inconvénients :**
- Un peu plus complexe à maîtriser au début :contentReference[oaicite:2]{index=2}

---

## 🔹 C’est quoi un _commit_ ?
Un **commit** est un **snapshot** (capture) de ton projet à un instant donné, avec :
- un message,
- un identifiant unique (SHA),
- des infos auteur/date.

Chaque commit devient une étape dans l’historique que tu peux consulter ou revenir à plus tard. :contentReference[oaicite:3]{index=3}

---

## 🔹 Comment configurer Git ?
Avant de commencer :
```bash
git config --global user.name "Ton Nom"
git config --global user.email "email@example.com"
````

Tu peux aussi configurer l’éditeur par défaut :

```bash
git config --global core.editor "code --wait"
```

Ces infos seront attachées à tes commits.

---

## 🔹 C’est quoi une *branche* ?

Une **branche** est une **ligne de développement indépendante**.

* Tu peux créer une branche pour une fonctionnalité, tester, puis l’intégrer ensuite dans la branche principale.
* Chaque branche a son propre historique à partir du point de création. ([Medium][1])

---

## 🔹 C’est quoi les *staging areas* ?

La **staging area** (aussi appelée *index*) est une **zone intermédiaire** où tu choisis exactement quelles modifications tu veux **inclure dans le prochain commit**.

* Tu édites des fichiers → ils restent modifiés dans ton dossier.
* Tu fais `git add` → les changements vont dans la **staging area**.
* Tu fais `git commit` → Git crée un commit avec les éléments de la staging area. ([yanickvanweydeveldt.com][2])

---

## 🧾 Résumé super court

| Concept      | Court                  |
| ------------ | ---------------------- |
| Git          | VCS distribué          |
| Commit       | Snapshot versionné     |
| Branche      | Ligne de développement |
| Staging area | Zone avant commit      |

```