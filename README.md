# Estimation et Validation du Modèle à 5 Facteurs de Fama-French

Ce projet porte sur l'estimation et le test du modèle à 5 facteurs de Fama-French. Ce modèle est un cadre populaire dans la finance pour expliquer les variations des rendements des portefeuilles d'actifs en fonction de plusieurs facteurs systématiques.

## Objectifs

1. Estimer les coefficients du modèle de Fama-French à 5 facteurs pour des portefeuilles d'actions cotées sur le NYSE, AMEX et Nasdaq.
2. Évaluer dans quelle mesure ces facteurs expliquent les variations des rendements anticipés.
3. Tester l'ajustement du modèle sur la période **1963-07-01** à **2024-09-01**.

## Données Utilisées

Les données des facteurs de Fama-French ont été récupérées depuis [la bibliothèque de Kenneth French](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html). Elles incluent les séries mensuelles des facteurs suivants :

- **Mkt-RF** : Rendement du marché corrigé par le taux sans risque.
- **SMB** : Différence des rendements entre les petites et grandes entreprises.
- **HML** : Différence des rendements entre les entreprises à fort et faible ratio valeur comptable/valeur de marché.
- **RMW** : Différence entre les rendements des entreprises à forte et faible rentabilité.
- **CMA** : Différence entre les rendements des entreprises conservatrices (faibles investissements) et agressives (forts investissements).
- **RF** : Taux sans risque.

## Étapes du Projet

1. **Importation des Données** :
   - Charger les données des facteurs Fama-French à partir du fichier CSV `F-F_Research_Data_5_Factors_2x3.csv`.
   - Vérifier les valeurs manquantes et nettoyer les données si nécessaire.

2. **Estimation du Modèle** :
   - Décomposer les rendements des portefeuilles en fonction des cinq facteurs.
   - Estimer les coefficients $\beta_i$ pour chaque facteur à l'aide de régressions linéaires multiples.

3. **Analyse des Résultats** :
   - Vérifier si les coefficients estimés sont statistiquement significatifs.
   - Valider si $\alpha_i = 0$, ce qui indique que les facteurs expliquent les variations des rendements anticipés.

4. **Validation sur Période Étendue** :
   - Répéter l'analyse sur la période **1963-07-01** à **2024-09-01** pour valider la robustesse du modèle.


