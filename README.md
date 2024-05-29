# Projet Data Science / Git : Analyse et Modélisation

L'objectif de ce projet est de vous familiariser avec les outils et les processus utilisés en data science, y compris l'analyse exploratoire des données (EDA), le prétraitement des données, l'ingénierie des caractéristiques, l'entraînement de modèles de machine learning, et l'utilisation de Git et GitHub pour la collaboration en équipe.

## Détail de l'attendu et des preprocessing / analyses et modélisations attendues :

### 1. Nettoyage des Données

Le nettoyage des données est une étape fondamentale pour garantir l'intégrité et la qualité des données utilisées dans les analyses et les modèles. Voici les tâches spécifiques de nettoyage à effectuer :

- **Gestion des valeurs manquantes :** Identifier et traiter les valeurs manquantes dans les jeux de données clients, produits et transactions. Cela peut inclure l'imputation des valeurs manquantes ou la suppression des enregistrements incomplets.
- **Correction des incohérences :** Rechercher et corriger les incohérences dans les données, telles que des dates invalides, des doublons ou des valeurs aberrantes.
- **Standardisation des formats :** Uniformiser les formats des données (dates, numéros de téléphone, adresses, etc.) pour assurer une cohérence à travers l'ensemble des jeux de données.
- **Nettoyage des textes :** Pour les données textuelles (noms de produits, descriptions, etc.), effectuer un nettoyage des textes pour éliminer les fautes de frappe, les caractères spéciaux indésirables et les espaces superflus.
- **Vérification des relations entre les jeux de données :** S'assurer que les relations entre les clients, les produits et les transactions sont logiques et cohérentes.

### 2. Exploration des Données

L'exploration des données permet de comprendre les caractéristiques et les tendances des jeux de données. Voici quelques analyses intéressantes à réaliser :

- **Analyse descriptive :** Calculer des statistiques descriptives (moyenne, médiane, écart-type, etc.) pour chaque jeu de données afin de résumer les principales caractéristiques.
- **Visualisation des données :** Utiliser des graphiques et des visualisations pour identifier des tendances, des distributions et des anomalies dans les données. Par exemple, des histogrammes pour les ventes de produits, des diagrammes de dispersion pour les relations entre variables, etc.
- **Analyse des segments de clients :** Identifier des segments de clients basés sur des critères démographiques ou comportementaux, et analyser leurs caractéristiques.
- **Analyse des transactions :** Étudier les tendances des transactions, comme les périodes de forte activité, les produits les plus vendus, etc.
- **Analyse des corrélations :** Rechercher des corrélations entre différentes variables pour identifier des relations potentielles à explorer plus en profondeur lors de la modélisation.

### 3. Modélisation des Données

La modélisation des données implique le développement de modèles prédictifs et descriptifs pour répondre à des questions business spécifiques. Voici quelques approches de feature engineering et de modélisation à considérer :

- **Feature Engineering :**
  - **RFM (Récence, Fréquence, Montant) :** Calculer les scores RFM pour chaque client afin de segmenter la clientèle en fonction de la récence de leurs achats, de la fréquence de leurs transactions et du montant dépensé / Pour le calcul de la recency vous pouvez utiliser la date la plus récente du dataset plutot que la date d'aujourd'hui.
  - **Segmentation comportementale :** Créer des segments de clients basés sur des comportements d'achat, tels que les catégories de produits préférées, la saisonnalité des achats, etc.
  - **Variables dérivées :** Créer de nouvelles variables à partir des données existantes, comme le nombre moyen de transactions par mois, la valeur moyenne des transactions, etc.

- **Objectif de la Segmentation :**
  - **Personnalisation des campagnes marketing :** Utiliser la segmentation pour cibler des groupes de clients spécifiques avec des offres personnalisées, ce qui peut améliorer l'efficacité des campagnes marketing.
  - **Amélioration de la fidélisation :** Identifier les clients à risque de churn (désabonnement) et développer des stratégies pour les fidéliser.
  - **Optimisation des assortiments de produits :** Adapter les assortiments de produits en fonction des préférences des différents segments de clients.
  - **Prévision des ventes :** Utiliser les segments de clients pour améliorer les prévisions de ventes et optimiser les stocks.

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

- Le notebook `notebooks/modeling.ipynb` peut-être utilisé pour tester le feature engineering
- Utilisez `src/feature_engineering.py` pour automatiser si vous le voulez à l'aide de fonctions la création des caractéristiques pertinentes.
- Cette étape peut inclure la création de nouvelles variables à partir des données existantes.

### 4. Entraînement du Modèle

- Le notebook `notebooks/modeling.ipynb` peut-être utilisé pour entrainer et evaluer le modele
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



