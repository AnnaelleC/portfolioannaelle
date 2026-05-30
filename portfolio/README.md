# PortfolioAnnaelle - Lancement dans GitHub Codespaces

Ce projet est un site **HTML/CSS/JS pur**.  
Dans GitHub Codespaces, il est plus pratique d’utiliser un petit serveur local pour pouvoir ouvrir le site via un port.

## Prérequis pour le bon fonctionnement de ce site Web

- Un Codespace créé à partir de ce dépôt.
- Node.js installé dans le Codespace (normalement déjà présent).

## Démarrage rapide

1. Ouvrir un terminal dans le Codespace  
   - Menu : `Terminal` → `New Terminal`.

2. Installer le serveur statique `serve` (une seule fois) :

   ```bash
   npm install -g serve
   ```

3. Aller dans le dossier qui contient index.html (si c'est le cas, sinon pas besoin d'aller dans un dossier):

   ```bash
   cd nomDossier
   ```

4. Lancer le serveur sur le port 3000 :

   ```bash
   serve -l 3000 
   ```

5. Ouvrir le site dans le navigateur :

    - En bas de VS Code, onglet PORTS.
    - Repérer le port 3000.
    - Cliquer sur l’icône de globe (Open in Browser).

   ```bash
   Le site s’ouvrira alors dans un nouvel onglet de ton navigateur, servi directement depuis le Codespace.
   ```
6. Architecture du projet :

   ```
   portfolio/
   ├── index.html              ← Point d'entrée principal
   ├── README.md
   │
   ├── css/
   │   ├── style.css           ← Styles globaux (variables, nav, hero, sections, responsive)
   │   └── chatbot.css         ← Styles du chatbot IA
   │
   ├── js/
   │   ├── main.js             ← Curseur Wii, thème clair/sombre, animations, nav, formulaire
   │   └── chatbot.js          ← Réponses du bot, navigation par section, avatar robot
   │
   └── sections/
      ├── projets.html        ← Les 4 projets (Pic du Midi, Intégration, Commande, Fâ)
      ├── competences.html    ← CV, formation, grille de compétences
      ├── stages.html         ← Stage FEBUS OPTICS + Stage ARGITIK
      ├── veille.html         ← Veille Cybersécurité + Veille Snyk
      ├── contact.html        ← Infos contact + formulaire
      └── chatbot.html        ← HTML du bouton flottant et fenêtre chat
   ```

Fix rapide (En cas de probleme de push) : a

```bash
git config pull.rebase true
git pull origin main
Ça rebase tes changements locaux au-dessus des remote (histoire linéaire, propre pour GitHub Pages).
​

Alternative merge (si tu préfères garder historique) :

bash
git config pull.ff only
git pull --no-rebase origin main
```

## Commandes Git essentielles

### Vérifier l’état du dépôt

```bash id="qk2v7n"
git status
```

---

### Ajouter les fichiers

```bash id="m9v1sa"
git add .
```

---

### Faire un commit

```bash id="c8x2lp"
git commit -m "message"
```

---

### Envoyer sur GitHub

```bash id="z1d6rq"
git push origin main
```

---

## Problèmes fréquents

### Commit bloqué (erreur GPG ou signature)

```bash id="t5k0vn"
git commit --no-gpg-sign -m "message"
```

Désactiver la signature :

```bash id="b3m8qa"
git config --global commit.gpgsign false
```

---

### Problème lors d’un pull

Solution recommandée :

```bash id="h7p1xd"
git pull --rebase origin main
```

Solution classique :

```bash id="l4c9we"
git pull origin main
```

---

### Changer de branche

```bash id="u9n3qx"
git branch
git switch nom_branche
```

---

## Réinitialisation

Annuler des modifications locales :

```bash id="r2m8ty"
git restore nom_fichier
```

Réinitialisation complète (attention) :

```bash id="f6x1qp"
git reset --hard
```

---

## Bonnes pratiques

* Vérifier `git status` avant chaque commit
* Sauvegarder les fichiers avant Git (Ctrl + S)
* Faire des commits réguliers et clairs
* Ne pas pousser de code cassé sur main

---

## Problèmes d’affichage dans Codespaces

Si le site ne s’ouvre pas :

* Vérifier que le port 3000 est ouvert
* Relancer `serve -l 3000`
* Vérifier que le terminal est dans le bon dossier

---

## Objectif du projet

Ce portfolio a pour objectif de :

* présenter des projets BTS SIO
* démontrer des compétences en développement web
* structurer un projet complet utilisable en contexte professionnel
