# 📊 Analyse Statistique des Diplômés de l'Enseignement Supérieur Public Tunisien

[![Quarto](https://img.shields.io/badge/Made%20with-Quarto-blue.svg)](https://quarto.org/)
[![R](https://img.shields.io/badge/R-276DC3?logo=r&logoColor=white)](https://www.r-project.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> Analyse approfondie de la répartition des 55,670 diplômés de l'enseignement supérieur public en Tunisie (2021-2022)

## 🎯 Objectifs du Projet

Ce projet présente une analyse statistique complète et interactive de la production de diplômés en Tunisie, structurée autour de **6 axes d'analyse** :

1. **📈 Répartition par Genre** - Analyse du déséquilibre F/M et identification des domaines les plus genrés
2. **⚠️ Domaines Saturés** - Identification des concentrations excessives via analyse de Pareto
3. **🏛️ Performance des Établissements** - Classement et profils des établissements universitaires
4. **🎓 Domaine × Diplôme** - Analyse croisée de la structure académique
5. **🔬 Analyse Multivariée** - ACP et clustering K-means pour identifier les profils types
6. **💼 Mismatch Académique** - Évaluation du risque de décalage offre/demande

## 📊 Données

- **Source** : [Catalogue Open Data Tunisie](https://catalog.data.gov.tn/fr/dataset/les-etudiants-diplomes-des-universites-en-2021-2022)
- **Année académique** : 2021-2022
- **Organisme** : Ministère de l'Enseignement Supérieur et de la Recherche Scientifique
- **Données** :
  - 55,670 diplômés au total
  - 14 universités
  - 189 établissements
  - 22 domaines d'étude
  - 2,083 observations finales

## 🏗️ Structure du Projet

```
Higher-Education-Graduates-Analysis/
├── presentation.qmd           # Présentation Quarto interactive principale
├── custom.scss               # Thème SCSS personnalisé
├── styles.css               # Styles CSS additionnels
├── dataset/
│   ├── raw/                 # Données brutes (Excel)
│   │   ├── fact_diplomes.xls
│   │   ├── uni_code.xls
│   │   ├── etablissment_code.xls
│   │   ├── domaines_code.xls
│   │   └── diplomes_code.xls
│   └── merged/              # Données fusionnées (CSV)
│       └── diplomes_fusionnes.csv
├── notebooks/
│   └── Analyse_Statistique.ipynb  # Notebook d'exploration
├── img/                     # Images et logos
└── README.md               # Ce fichier

```

## 🚀 Installation et Utilisation

### Prérequis

- **R** (version ≥ 4.0)
- **Quarto** (version ≥ 1.4)
- **RStudio** (optionnel mais recommandé)

### Installation des packages R

```r
install.packages(c(
  "readxl",      # Lecture fichiers Excel
  "dplyr",       # Manipulation de données
  "tidyr",       # Nettoyage de données
  "ggplot2",     # Visualisations
  "knitr",       # Rapports dynamiques
  "gt",          # Tableaux élégants
  "plotly",      # Graphiques interactifs
  "DT"           # Tableaux interactifs filtrables
))
```

### Générer la présentation

```bash
# Prévisualisation en direct
quarto preview presentation.qmd

# Générer le fichier HTML final
quarto render presentation.qmd
```

Le fichier généré sera : `presentation.html`

## 📈 Méthodologies Statistiques

- **Analyse descriptive** : Distributions, moyennes, pourcentages
- **Tableaux de contingence** : Analyse croisée domaine × diplôme
- **Diagramme de Pareto** : Identification des concentrations (principe 80/20)
- **ACP (Analyse en Composantes Principales)** : Réduction de dimensionnalité
- **Clustering K-means** : Segmentation automatique en 4 groupes
- **Indice de Herfindahl-Hirschman** : Mesure de concentration

## 🎨 Fonctionnalités Interactives

- ✅ **Navigation fluide** entre les slides avec transitions animées
- ✅ **Graphiques interactifs Plotly** avec tooltips et zoom
- ✅ **Tableau filtrable DT** pour exploration des données
- ✅ **Diagrammes Mermaid** pour l'architecture des données
- ✅ **Code pliable** pour consultation des scripts R
- ✅ **Thème personnalisé** avec palette de couleurs cohérente

## 📊 Principaux Résultats

### Déséquilibre de Genre
- **Ratio F/H** : 2.33:1 (70% femmes, 30% hommes)
- Domaines fortement genrés identifiés

### Concentration Académique
- **Top 5 domaines** : ~60% des diplômés
- **Top 10 domaines** : ~85% des diplômés
- **Indice Herfindahl** : Concentration modérée à forte

### Clustering
- **4 profils distincts** identifiés par K-means
- Segmentation basée sur volume, genre, et diversité

### Risque de Mismatch
- Surproduction potentielle dans certains domaines
- Nécessité d'ajuster l'offre de formation

## 🎓 Auteur

**Abderrahmen Youssef**   
Janvier 2026

---
