# Prédiction des Ventes Kaggle - Playground Series S5E1

## Présentation du Projet
Ce projet vise à prédire les ventes de divers autocollants de marque Kaggle provenant de différents magasins fictifs dans plusieurs pays réels sur plusieurs années. Le jeu de données est synthétique mais reflète des modèles de données du monde réel tels que la saisonnalité, les jours fériés et les effets du week-end.

## Description du Jeu de Données
Le jeu de données se compose de trois fichiers :
- `train.csv` : Données de ventes avec les colonnes `date`, `country`, `store`, `product` et la variable cible `num_sold`.
- `test.csv` : Structure similaire sans la variable cible ; l'objectif est de prédire `num_sold` pour chaque ligne.
- `sample_submission.csv` : Exemple de format de soumission des prédictions.

## Flux de Travail du Projet
### 1. Chargement et Exploration des Données
- Chargement des jeux de données avec Pandas.
- Visualisation des données avec Matplotlib et Seaborn.
- Identification et gestion des valeurs manquantes.

### 2. Ingénierie des Variables (Feature Engineering)
- Conversion de la date en plusieurs caractéristiques : année, mois, jour, jour de la semaine, week-end.
- Création d'une variable saisonnière basée sur le mois.
- Encodage des variables catégorielles avec `one-hot encoding`.
- Normalisation des caractéristiques numériques avec `StandardScaler`.

### 3. Séparation des Données
- Division des données d'entraînement en ensembles d'entraînement et de validation avec `train_test_split`.

### 4. Sélection et Entraînement des Modèles
- Test de plusieurs modèles :
  - Random Forest Regressor
  - Gradient Boosting Regressor
  - Linear Regression
  - Support Vector Regressor
- Évaluation des modèles à l'aide du RMSE et sélection du meilleur modèle.

### 5. Optimisation des Hyperparamètres
- Optimisation du meilleur modèle (Random Forest) à l'aide de la validation croisée par grille (`GridSearchCV`).

### 6. Prédictions Finales et Soumission
- Génération des prédictions sur l'ensemble de test.
- Enregistrement des résultats dans un fichier `submission.csv` prêt pour la soumission sur Kaggle.

## Outils et Bibliothèques Utilisés
- Python
- Pandas
- Scikit-Learn
- Matplotlib
- Seaborn

## Instructions d'Exécution
1. Charger les jeux de données depuis Kaggle.
2. Exécuter toutes les cellules du notebook fourni.
3. Le fichier final de soumission `submission.csv` sera généré.

## Licence
Ce projet est destiné à des fins éducatives dans le cadre de la série Playground de Kaggle.

