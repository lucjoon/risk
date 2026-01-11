# Instructions pour mettre en ligne sur GitHub

## Méthode 1 : Token d'accès personnel (Recommandé)

1. **Créer un token GitHub** :
   - Allez sur : https://github.com/settings/tokens
   - Cliquez sur "Generate new token" → "Generate new token (classic)"
   - Nom : `risk-project` (ou autre nom)
   - Cochez la case `repo`
   - Cliquez sur "Generate token"
   - **Copiez le token immédiatement** (il ne sera affiché qu'une fois !)

2. **Pousser le code** :
   Dans le terminal, exécutez :
   ```bash
   git push -u origin main
   ```
   
   Quand on vous demande votre nom d'utilisateur : entrez `lucjoon`
   Quand on vous demande votre mot de passe : **collez votre token** (pas votre mot de passe GitHub)

## Méthode 2 : Utiliser SSH (Alternative)

Si vous préférez utiliser SSH :

1. **Générer une clé SSH** (si vous n'en avez pas) :
   ```bash
   ssh-keygen -t ed25519 -C "votre_email@example.com"
   ```
   (Appuyez sur Entrée pour accepter les valeurs par défaut)

2. **Ajouter la clé SSH à GitHub** :
   - Affichez votre clé publique :
     ```bash
     cat ~/.ssh/id_ed25519.pub
     ```
   - Copiez le contenu
   - Allez sur : https://github.com/settings/keys
   - Cliquez sur "New SSH key"
   - Collez la clé et sauvegardez

3. **Changer le remote vers SSH** :
   ```bash
   git remote set-url origin git@github.com:lucjoon/risk.git
   git push -u origin main
   ```

## Après le push - Activer GitHub Pages

Une fois le code poussé sur GitHub :

1. Allez sur votre dépôt : https://github.com/lucjoon/risk
2. Cliquez sur **Settings** (en haut du dépôt)
3. Dans le menu de gauche, cliquez sur **Pages**
4. Sous "Source", sélectionnez **"Deploy from a branch"**
5. Choisissez **"main"** comme branche et **"/ (root)"** comme dossier
6. Cliquez sur **"Save"**

Votre site sera disponible à :
**https://lucjoon.github.io/risk/**

Le déploiement peut prendre 1-2 minutes.

