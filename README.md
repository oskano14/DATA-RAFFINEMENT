# ☕ Projet Data Refinement : Cafe Sales Analysis

Ce projet réalise le nettoyage et l'enrichissement d'un dataset de ventes de café ("Dirty Cafe Sales") contenant des erreurs intentionnelles, dans le cadre du module Data Refinement.

## 📂 Structure du Projet

L'architecture respecte les bonnes pratiques de Data Engineering :

- **DATA/**
  - `RAW/` : Contient le fichier original `dirty_cafe_sales.csv` (10 000 lignes).
  - `PROCESSED/` : Contient les fichiers nettoyés `cleaned_cafe_sales.csv` et enrichis.
- **NOTEBOOKS/**
  - `01_EXPLORATION.ipynb` : Audit des données (détection des 30% de valeurs manquantes et des erreurs "ERROR"/"UNKNOWN").
  - `02_CLEANING.ipynb` : Script de nettoyage avancé.
    - *Stratégie :* Imputation des lieux inconnus, déduction des articles via le prix (Logique Métier), et correction des totaux.
    - *Résultat :* 99.2% des données conservées.
  - `03_TRANSFORMATION.ipynb` : Feature Engineering.
    - Ajout de la saisonnalité (Mois/Jour) et segmentation des prix (Low/High Cost).
- **REPORTS/**
  - `RAPPORT.pdf` : Analyse détaillée et justification des choix méthodologiques.

## 🛠️ Installation

1. Cloner le projet.
2. Installer les dépendances :
   ```bash
   pip install -r requirements.txt