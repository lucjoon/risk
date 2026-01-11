# Comment créer un token GitHub - Guide étape par étape

## 📝 Étapes détaillées

### 1. Se connecter à GitHub
- Allez sur [github.com](https://github.com) et connectez-vous avec votre compte (`lucjoon`)

### 2. Accéder aux paramètres des tokens
- Cliquez sur votre **photo de profil** en haut à droite
- Cliquez sur **Settings** (Paramètres)

### 3. Aller dans la section Developer settings
- Dans le menu de gauche, faites défiler jusqu'à la section **Developer settings**
- Cliquez sur **Developer settings**

### 4. Accéder aux Personal access tokens
- Dans le menu de gauche, cliquez sur **Personal access tokens**
- Cliquez sur **Tokens (classic)** (ou **Fine-grained tokens** si vous préférez, mais classic est plus simple)

### 5. Créer un nouveau token
- Cliquez sur le bouton **Generate new token**
- Choisissez **Generate new token (classic)**

### 6. Configurer le token
Remplissez le formulaire :

- **Note** (Nom) : Donnez un nom au token, par exemple : `risk-project` ou `projet-risk`
- **Expiration** : Choisissez une durée (90 jours, 1 an, ou "No expiration" si vous voulez qu'il n'expire jamais)
- **Select scopes** (Permissions) : Cochez au minimum :
  - ✅ **`repo`** (Full control of private repositories)
    - Cela inclut automatiquement toutes les permissions nécessaires pour pousser du code

### 7. Générer et copier le token
- Faites défiler vers le bas et cliquez sur le bouton vert **Generate token**
- **⚠️ IMPORTANT** : Le token s'affichera UNE SEULE FOIS
- **COPIEZ-LE IMMÉDIATEMENT** et mettez-le dans un endroit sûr
- Il ressemblera à quelque chose comme : `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`

### 8. Utiliser le token

Une fois que vous avez le token :

1. Ouvrez un terminal dans le dossier de votre projet
2. Exécutez :
   ```bash
   git push -u origin main
   ```
3. Quand il vous demande :
   - **Username** : entrez `lucjoon`
   - **Password** : **collez votre token** (pas votre mot de passe GitHub !)

---

## 🎯 Raccourci direct

Vous pouvez aussi aller directement à cette URL une fois connecté :
👉 https://github.com/settings/tokens/new

---

## ⚠️ Sécurité

- **Ne partagez JAMAIS votre token**
- **Ne le committez JAMAIS dans votre code**
- Si vous pensez qu'il a été compromis, supprimez-le et créez-en un nouveau
- Vous pouvez voir tous vos tokens dans : https://github.com/settings/tokens

---

## 🔄 Alternative : GitHub CLI (plus simple mais nécessite une installation)

Si vous installez GitHub CLI (`gh`), vous pouvez vous authentifier plus facilement :
```bash
brew install gh
gh auth login
```

Mais pour l'instant, le token est la méthode la plus simple !

