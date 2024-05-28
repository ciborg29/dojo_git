# Projet Data Science / Git : Analyse et Modélisation

## Objectif du Dojo

L'objectif de ce projet est de vous familiariser avec les outils et les processus utilisés en data science, y compris l'analyse exploratoire des données (EDA), le prétraitement des données, l'ingénierie des caractéristiques, l'entraînement de modèles de machine learning, et l'utilisation de Git et GitHub pour la collaboration en équipe.

## Structure du Projet

Le projet est structuré comme suit :
```
project/
├── data/ # Dossiers pour les datasets
│ └── raw/ # Données brutes
│ └── processed/ # Données traitées
├── notebooks/ # Notebooks Jupyter pour l'analyse
│ └── cleaning.ipynb
│ └── exploration.ipynb
│ └── modeling.ipynb
├── src/ # Scripts source Python
│ └── data_preprocessing.py
│ └── feature_engineering.py
│ └── model_training.py
├── README.md # Documentation du projet
└── .gitignore # Fichiers à ignorer par Git
```
## Étapes du Projet

### 0. Nettoyage des données
- Utiliser le dataset présent dans `data/raw` et le nettoyer dans `notebooks/cleaning.ipynb`
- Assurez-vous de gérer les valeurs manquantes, de normaliser les données, et d'effectuer toute autre étape nécessaire pour préparer les données pour l'analyse.
- Vous pouvez créer de nouvelles variables qui vous semblent pertinentes

### 1. Exploration des Données

- Utilisez le notebook `notebooks/exploration.ipynb` pour effectuer une analyse exploratoire des données (EDA).
- Visualisez les distributions des données, identifiez les valeurs manquantes, et explorez les relations entre les variables.
- Vous pouvez utiliser la librairie de visualisations graphique de votre choix numpy, seaborn, plotly...

### 2. Prétraitement des Données

- Une fois le nettoyage réalisé sur `notebooks/cleaning.ipynb` vous pouvez le mettre en place dans le script (facultatif) en utilisant des fonctions.
- Si vous avez le temps ou décider de le faire vous pouvez écrire le code pour nettoyer et préparer les données dans `src/data_preprocessing.py`.
- Assurez-vous de gérer les valeurs manquantes, de normaliser les données, et d'effectuer toute autre étape nécessaire pour préparer les données pour l'analyse.

### 3. Ingénierie des Caractéristiques -> liée à la mosélisation

- Le notebook `modeling.ipynb` peut-être utilisé pour tester le feature engineering
- Utilisez `src/feature_engineering.py` pour automatiser si vous le voulez à l'aide de fonctions la création des caractéristiques pertinentes.
- Cette étape peut inclure la création de nouvelles variables à partir des données existantes.

### 4. Entraînement du Modèle

- Le notebook `notebooks/model_training.ipynb` peut-être utilisé pour entrainer et evaluer le modele
- Comparez les performances des modèles et sélectionnez le meilleur modèle en fonction des métriques d'évaluation.
- Une fois satisfait du modèle vous pouvez automatiser l'entrainement et la prediction du modèle dans `src/model_training.py`.


## Collaboration en Équipe

1. **Formation des Groupes** : Vous serez formés en groupes de 3 à 4 élèves.
2. **Fork du Dépôt** : Un élève par groupe doit forker ce dépôt et inviter les deux autres membres en tant que collaborateurs, une fois ajouté au dépot vous pouvez cloner le projet sur un repertoire en local.
   
2.1. **Comment inviter des personnes sur un repo** :

https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-teams-and-people-with-access-to-your-repository

2.2. **Comment Fork un projet** :

https://www.freecodecamp.org/news/how-to-fork-a-github-repository/

4. **Branches** : Chaque élève doit travailler sur une branche dédiée :
   - `feature-data-cleaning` pour le prétraitement des données/nettoyage
   - `feature-vizualization` pour la partie exploration des données
   - `feature-model-training` pour le feature engineering et l'entraînement des modèles
5. **Commit et Push** Chaque fois que vous etes satisfait de l'avancement de votre travail vous pouvez commit les modifs réalisées et ensuite push sur la branche associée du repo distant


** BONUS **

Ressources pour les pull requests : 

https://www.frayssinet.org/2021/06/25/tuto-debutant-faire-une-pull-request-sur-github-avec-git/
   
6. **Pull Requests** : Une fois le travail terminé, créez des pull requests (PR) de vos branches vers la branche principale du fork.
7. **Revue de Code** : Les autres membres du groupe doivent revoir les PRs, fournir des commentaires, et approuver les changements.
8. **Pull Request Finale** : Après approbation de toutes les PRs internes, créez une PR finale du fork vers le dépôt initial.



