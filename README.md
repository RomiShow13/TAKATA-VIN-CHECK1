# Takata VIN Check (GitHub Pages)

Une mini-page web pour vérifier rapidement si un modèle/année contient des rappels liés aux **airbags Takata** (via API publiques NHTSA) et obtenir le **lien constructeur officiel** pour le statut VIN exact en Europe/France.

## Déploiement rapide sur GitHub Pages

### 1) Crée le dépôt
- Sur GitHub, clique **New repository** → Nom : `takata-vin-check` (au choix) → Public → **Create repository**.

### 2) Ajoute les fichiers
**Option A (glisser-déposer via interface)**  
- Ouvre ton dépôt → onglet **Code** → bouton **Add file** → **Upload files**.  
- Glisse **index.html** et **.nojekyll** (fichier vide) à la racine → **Commit changes**.

**Option B (Git en ligne de commande)**
```bash
git clone https://github.com/<ton-compte>/<ton-repo>.git
cd <ton-repo>
# Copie index.html et .nojekyll dans ce dossier
git add index.html .nojekyll
git commit -m "Initial commit: Takata VIN Check"
git push origin main
```

### 3) Active GitHub Pages
- Va dans **Settings** → **Pages**.  
- **Source** : *Deploy from a branch*  
- **Branch** : `main` / **root** (`/`) → **Save**.  
- Attends ~30 secondes → l’URL s’affiche (ex: `https://<ton-compte>.github.io/<ton-repo>/`).

### 4) Utilisation
- Ouvre l’URL sur ton iPhone → bouton **Partager** → **Ajouter à l’écran d’accueil**.  
- Saisis un **VIN** (17 caractères) → vérifie les mentions **Takata** et utilise le **lien constructeur** pour confirmer le statut VIN exact.

## Notes importantes
- **NHTSA vPIC + Recalls** : rappels *par modèle/année* — ne confirment pas seuls le statut *par VIN*. Utilise le lien officiel du **constructeur** pour l’Europe/FR.  
- Historique local (8 derniers VIN) stocké dans le navigateur.  
- Aucune donnée perso envoyée vers un serveur — appels API directs depuis ton navigateur.

## Améliorations possibles
- Mode **PWA** (icône, cache offline, splash)  
- **Export CSV** de l’historique  
- Bouton **Scan VIN** via l’appareil photo (si besoin)

—
Fait pour un déploiement simple et propre ✌️
