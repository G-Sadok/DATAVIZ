# 🏠 House Prices: Exploratory Data Analysis (EDA)

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-76B900?style=for-the-badge&logo=python&logoColor=white)
![YData Profiling](https://img.shields.io/badge/YData_Profiling-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

## 📖 Aperçu du Projet

Ce projet est une **Analyse Exploratoire de Données (EDA)** complète menée sur le dataset *House Prices*. L'objectif est de comprendre la structure des données, d'identifier les variables clés influençant le prix de vente (`SalePrice`) et de nettoyer le jeu de données en vue d'une modélisation prédictive future.

L'analyse combine une approche automatisée (génération de rapports) et une exploration manuelle approfondie (nettoyage, visualisations statistiques).

## 📂 Structure du Projet

* **`analysis.ipynb`** : Le cœur de l'analyse. Contient le code Python pour le chargement, le nettoyage, la visualisation et l'étude des corrélations.
* **`report.html`** : Rapport complet généré automatiquement par *YData Profiling*, offrant une vue d'ensemble instantanée des distributions et des alertes sur les données.
* **`exploratory-data-analysis-CA-2.pdf`** : Instructions et contexte du projet.

## 🛠️ Méthodologie et Étapes Clés

### 1. Profilage Automatisé
Utilisation de la bibliothèque `ydata-profiling` pour générer un audit complet du dataset :
* Détection des types de données.
* Identification des valeurs manquantes et des doublons.
* Analyse statistique descriptive (moyenne, médiane, écart-type) pour chaque colonne.

### 2. Nettoyage des Données (Data Cleaning)
Sur la base du rapport et de l'analyse manuelle :
* **Gestion des `Null` :** Suppression des colonnes contenant une trop grande proportion de valeurs manquantes (ex: `PoolQC`, `MiscFeature`, `Alley`) qui n'apportent pas d'information fiable.
* **Traitement des ID :** Suppression de la colonne `Id` car non pertinente pour la prédiction.

### 3. Analyse des Corrélations
* **Heatmap :** Création d'une matrice de corrélation (Seaborn) pour visualiser les liens entre les variables numériques.
* **Identification des Features :** Mise en évidence des variables ayant la plus forte corrélation positive avec `SalePrice` (ex: `OverallQual`, `GrLivArea`).

### 4. Visualisation
* **Scatter Plots :** Tracé de graphiques (ex: `SalePrice` vs `GrLivArea`) pour confirmer visuellement les tendances linéaires et repérer les valeurs aberrantes (outliers).
* **Distribution :** Analyse de la variable cible `SalePrice`.



## 🚀 Installation et Utilisation

1.  **Cloner le dépôt :**
    ```bash
    git clone [https://github.com/ton-user/house-prices-eda.git](https://github.com/ton-user/house-prices-eda.git)
    cd house-prices-eda
    ```

2.  **Installer les dépendances :**
    ```bash
    pip install pandas numpy matplotlib seaborn ydata-profiling jupyter
    ```

3.  **Explorer le projet :**
    * Ouvrez `analysis.ipynb` avec Jupyter pour voir le code étape par étape.
    * Ouvrez `report.html` dans votre navigateur pour voir l'audit complet des données.

---

## 🇬🇧 English Summary

**Project:** House Prices Exploratory Data Analysis (EDA)

**Goal:** Perform a deep dive into the housing dataset to clean data and identify key drivers for sale prices.

**Key Features:**
* **Automated Profiling:** Generated a comprehensive HTML report using `ydata-profiling` for quick statistical overview.
* **Data Cleaning:** Removed high-missing-value columns (e.g., PoolQC) and irrelevant identifiers based on analysis.
* **Correlation Analysis:** Used Seaborn heatmaps to identify strong predictors like `OverallQual` and `GrLivArea`.
* **Visualization:** Created scatter plots to validate relationships between living area and price.

**Tech Stack:** Python, Pandas, Seaborn, YData Profiling.
