# Guide de Présentation

## 🎯 Structure de la présentation

Votre présentation Quarto interactive est organisée en **6 axes d'analyse principaux** :

1. **Axe 1 - Répartition par Genre** : Analyse F/M avec visualisations interactives
2. **Axe 2 - Domaines Saturés** : Diagramme de Pareto et concentration
3. **Axe 3 - Performance Établissements** : Classement et diversité
4. **Axe 4 - Domaine × Diplôme** : Analyses croisées
5. **Axe 5 - Analyse Multivariée** : ACP et K-means clustering
6. **Axe 6 - Mismatch Académique** : Risques et recommandations

## 🚀 Comment générer la présentation

### Option 1 : Via RStudio
```r
# Ouvrir le fichier presentation.qmd dans RStudio
# Cliquer sur "Render" ou utiliser :
quarto::quarto_render("presentation.qmd")
```

### Option 2 : Via Terminal
```bash
cd /home/abdou/Desktop/Higher-Education-Graduates-Analysis
quarto render presentation.qmd
```

### Option 3 : Preview en temps réel
```bash
quarto preview presentation.qmd
```

## 🎨 Fonctionnalités interactives

- **Navigation** : Flèches ← → ↑ ↓
- **Menu** : Touche `M` pour afficher le menu de navigation
- **Vue d'ensemble** : Touche `Esc` ou `O` pour la vue mosaïque
- **Recherche** : Ctrl+Shift+F (Windows/Linux) ou Cmd+Shift+F (Mac)
- **Chalkboard** : Icône en bas à gauche pour annoter
- **Zoom** : Alt+Click sur un élément
- **Plein écran** : Touche `F`

## 📊 Graphiques interactifs

Les graphiques utilisant `plotly` sont **entièrement interactifs** :
- Zoom : Sélectionner une zone
- Pan : Cliquer-glisser
- Hover : Informations détaillées
- Reset : Double-clic

## 🎭 Personnalisation

### Modifier les couleurs
Éditez `custom.scss` pour changer les couleurs principales :
```scss
$primary: #3b82f6;    // Bleu
$secondary: #8b5cf6;   // Violet
$success: #10b981;     // Vert
$danger: #ef4444;      // Rouge
$warning: #f59e0b;     // Orange
```

### Ajouter votre logo
Placez votre logo dans `/img/logo.png`

## 📤 Export

### En PDF
```bash
quarto render presentation.qmd --to pdf
```

### En HTML (standalone)
```bash
quarto render presentation.qmd --to revealjs --embed-resources
```

## 🎯 Navigation recommandée

1. **Introduction** → Contexte et problématique
2. **Partie 1** → Préparation des données (rapide)
3. **Partie 2** → Les 6 axes d'analyse (détaillé)
4. **Synthèse** → Résultats clés et implications
5. **Questions** → Slide finale interactive

## 💡 Astuces de présentation

- Utilisez les **fragments** (éléments qui apparaissent progressivement)
- Les **panel-tabset** permettent de basculer entre plusieurs vues
- Les **callout boxes** mettent en évidence les points importants
- Les graphiques **interactifs** engagent l'audience

## 🔧 Dépannage

### Si les données ne se chargent pas :
Vérifiez que le fichier `dataset/merged/diplomes_fusionnes.csv` existe.

### Si le rendu échoue :
```r
# Installer les packages manquants
install.packages(c("knitr", "kableExtra", "plotly"))
```

### Pour mettre à jour Quarto :
```bash
# Vérifier la version
quarto --version

# Sur Ubuntu/Debian
sudo apt update && sudo apt upgrade quarto
```

## 📱 Visualisation sur mobile

La présentation est **responsive** et s'adapte automatiquement aux écrans mobiles et tablettes.

## 🌐 Publication en ligne

### GitHub Pages
```bash
# Rendre la présentation
quarto render presentation.qmd

# Le fichier HTML est dans presentation.html
# Vous pouvez le publier sur GitHub Pages
```

### Quarto Pub
```bash
quarto publish quarto-pub presentation.qmd
```

Bon courage pour votre présentation ! 🎓
