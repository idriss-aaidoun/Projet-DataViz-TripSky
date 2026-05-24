# Projet Data Analysis & DataViz : Optimisation Stratégique de TripSky

## 📌 Contexte du Projet
Ce projet a été réalisé dans le cadre du **Projet Final d'Analyse et Visualisation de Données (2ème Année Cycle Ingénieur)**. 

**TripSky** est une agence de voyages insolites française qui propose des séjours thématiques axés sur trois piliers : l'Aventure, la Détente, et la Culture. L'objectif principal de cette étude est d'accompagner June, la directrice marketing, dans le pilotage de l'efficacité de ses investissements publicitaires pour optimiser l'année fiscale en cours.

---

## 🎯 Problématique Métier
> **Comment les dépenses publicitaires influencent-elles les réservations et les revenus selon les saisons afin d’optimiser l’allocation du budget marketing de TripSky ?**

---

## 📊 Structure du Projet
Le dépôt est organisé de la manière suivante :
* 📂 **`Projetdatviz.ipynb`** : Le Notebook Python principal contenant l'ensemble de la démarche technique d'exploration (Data Profiling), le nettoyage, le traitement des anomalies/outliers, l'analyse descriptive et la génération des visualisations (EDA et Graphique explicatif final).
* 📂 **`rapport_tripsky.tex`** : Le rapport final rédigé en LaTeX suivant rigoureusement le cycle de la donnée exigé (Problème, Description, Nettoyage, EDA, Insights, Recommandations).
* 📂 **`.gitignore`** : Fichier de configuration pour exclure les fichiers temporaires de compilation LaTeX et Python du versionnage Git.

---

## 🛠️ Méthodologie & Cycle de la Donnée
1. **Data Profiling & Exploration :** Audit des métadonnées des deux datasets sources (`Données entreprise` de $800 \times 5$ et `Données clients` de $801 \times 16$).
2. **Nettoyage de Données :** Normalisation de la casse textuelle (`.str.lower().str.strip()`), alignement des types temporels (`datetime64`) et traitement de l'outlier d'âge critique (4100 ans imputé par la médiane).
3. **Analyse Exploratoire (EDA) :** Modélisation du ROAS (Return On Ad Spend) quotidien et saisonnier, calcul du coefficient de corrélation linéaire de Pearson ($r = 0.11$) et tableaux croisés dynamiques.
4. **Visualisation Explicative :** Création d'un graphique à double axe vertical (*Dual-Axis Chart*) mettant en évidence graphiquement le décalage (*mismatch*) budgétaire de l'entreprise.

---

## 💡 Insights Majeurs & Recommandations
* **Insight 1 (Mismatch budgétaire) :** TripSky applique une enveloppe publicitaire linéaire et figée (~1 M€ par trimestre) alors que le marché est profondément saisonnier (l'Été et l'Hiver capturent près de 67% des ventes).
* **Insight 2 (Crise de qualité) :** Le score de satisfaction client (CSAT) global est extrêmement bas ($< 2.6/5$), chutant à $2.27/5$ au Printemps.
* **Recommandation 1 :** Réallocation agile de **40% du budget publicitaire** des saisons creuses (Printemps/Automne) vers les périodes à forte affluence (Été/Hiver) pour lisser le CPA et maximiser le ROAS.
* **Recommandation 2 :** Gel temporaire des campagnes du Printemps et lancement d'un audit de qualité sur l'offre locale pour freiner l'attrition client.

---

## 🚀 Comment exécuter le projet ?
1. Clonez ce dépôt privé sur votre machine locale.
2. Assurez-vous de disposer des bibliothèques Python requises : `pandas`, `numpy`, `matplotlib`, `seaborn`.
3. Lancez le fichier `Projetdatviz.ipynb` dans un environnement Jupyter Notebook ou Google Colab.

---
**Filière :** Sciences des Données & Ingénierie Décisionnelle