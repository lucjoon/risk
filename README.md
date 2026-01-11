# 🎲 Dés Risk - Simulateur de batailles Risk

Un simulateur de batailles interactif pour le jeu de société Risk, permettant de simuler des combats entre deux camps avec des dés.

## 🌐 Accès en ligne

🔗 **[Accéder au simulateur sur GitHub Pages](https://lucjoon.github.io/risk/)**

## 🚀 Fonctionnalités

### Configuration des armées
- **Attaquant** : Configurez le nombre de soldats (minimum 1) et le nombre de dés (1, 2 ou 3)
- **Défenseur** : Configurez le nombre de soldats (minimum 1) et le nombre de dés (1 ou 2)

### Fonctionnalité "Stop"
- Définissez un seuil de stop pour chaque camp (optionnel)
- La bataille s'arrête automatiquement lorsque l'un des camps atteint ou passe en dessous de son seuil de stop
- Permet de contrôler quand arrêter la bataille pour éviter des pertes excessives

### Règles du Risk
- **L'attaquant doit toujours laisser au moins 1 soldat en réserve**
  - Avec 3 soldats ou moins → maximum 2 dés
  - Avec 2 soldats → maximum 1 dé
  - Avec 1 soldat → ne peut plus attaquer (bataille terminée)

### Interface en temps réel
- Compteur de soldats restants affiché en haut à droite pendant la bataille
- Mise à jour en temps réel à chaque tour
- Résultat final avec le nombre de soldats restants et les pertes totales

### Sauvegarde automatique
- Les nombres de soldats restants sont automatiquement sauvegardés dans les champs de saisie après chaque bataille
- Permet de continuer la bataille depuis l'état actuel

## 📖 Comment utiliser

1. **Configurez les armées** :
   - Entrez le nombre de soldats pour l'attaquant et le défenseur
   - Sélectionnez le nombre de dés à utiliser pour chaque camp
   - (Optionnel) Définissez un seuil de stop pour chaque camp

2. **Lancez la bataille** :
   - Cliquez sur le bouton "Lancer les dés"
   - La bataille se déroule automatiquement tour par tour
   - Observez le compteur de soldats restants en temps réel

3. **Résultat** :
   - Le résultat final s'affiche avec le vainqueur
   - Les nombres de soldats restants sont sauvegardés automatiquement
   - Vous pouvez relancer une bataille avec les soldats restants

## 🎮 Règles de combat

- Les dés sont comparés par paires (meilleur dé contre meilleur dé)
- Le perdant de chaque comparaison perd 1 soldat
- La bataille continue jusqu'à ce que :
  - L'un des camps n'ait plus de soldats
  - L'attaquant n'ait plus qu'1 soldat (ne peut plus attaquer)
  - Un seuil de stop est atteint
  - 100 tours sont atteints (limite de sécurité)

## 🛠️ Technologies utilisées

- HTML5
- CSS3 (avec animations 3D pour les dés)
- JavaScript (ES6+)

## 📝 Notes

- Le simulateur suit les règles classiques du Risk
- L'interface est entièrement en français
- Compatible avec tous les navigateurs modernes

## 📄 Licence

Ce projet est fourni tel quel, sans garantie.
