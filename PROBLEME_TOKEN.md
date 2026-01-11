# Problème d'authentification - Solution

## ⚠️ Erreur 403 : Permission denied

Cela signifie que le token n'a probablement pas les bonnes permissions.

## ✅ Solution : Créer un nouveau token avec les bonnes permissions

### Étapes :

1. **Révoquer l'ancien token** (important pour la sécurité puisqu'il a été partagé) :
   - Allez sur : https://github.com/settings/tokens
   - Trouvez votre token "risk-project" (ou le nom que vous avez donné)
   - Cliquez sur **Delete**

2. **Créer un nouveau token** :
   - Allez sur : https://github.com/settings/tokens/new
   - **Note** : `risk-project-v2`
   - **Expiration** : 90 days (ou votre préférence)
   - **Scopes** : Cochez **IMPORTANTEMENT** :
     - ✅ **`repo`** (Full control of private repositories)
       - Cela inclut automatiquement : repo:status, repo_deployment, public_repo, repo:invite, security_events
   - Cliquez sur **Generate token**
   - **COPIEZ LE TOKEN**

3. **Utiliser le nouveau token** :

   Dans le terminal, exécutez :
   ```bash
   git push -u origin main
   ```
   
   Quand demandé :
   - **Username** : `lucjoon`
   - **Password** : **collez votre nouveau token**

## 🔐 Alternative : Utiliser SSH (Plus sécurisé)

Si vous préférez éviter les tokens :

1. **Générer une clé SSH** :
   ```bash
   ssh-keygen -t ed25519 -C "votre_email@example.com"
   ```
   (Appuyez sur Entrée 3 fois pour accepter les valeurs par défaut)

2. **Afficher votre clé publique** :
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```

3. **Ajouter la clé à GitHub** :
   - Copiez tout le contenu affiché (commence par `ssh-ed25519 ...`)
   - Allez sur : https://github.com/settings/keys
   - Cliquez sur **New SSH key**
   - Titre : `Mac` (ou votre ordinateur)
   - Collez la clé dans "Key"
   - Cliquez sur **Add SSH key**

4. **Changer le remote vers SSH** :
   ```bash
   git remote set-url origin git@github.com:lucjoon/risk.git
   git push -u origin main
   ```

---

## 📋 Vérification des permissions du token actuel

Si vous voulez vérifier pourquoi le token actuel ne fonctionne pas :
- Allez sur : https://github.com/settings/tokens
- Vérifiez que votre token a bien la permission **`repo`** cochée

