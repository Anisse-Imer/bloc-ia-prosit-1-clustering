# Clustering des données immobilières californiennes

Bloc IA - Prosit 1 : segmentation géographique et socio-économique du marché immobilier californien via KMeans.

## Dataset

California Housing (recensement 1990) — 20 640 block groups, 10 variables.

## Pipeline

1. **Imputation** : `total_bedrooms` (207 NaN) imputé via KNNImputer (k=5)
2. **Sélection** : `latitude`, `longitude`, `median_income`, `median_house_value`
3. **Standardisation** : StandardScaler (centrage-réduction)
4. **Clustering** : KMeans (k=6, choisi par méthode du coude / WCSS)

## Notebooks

| Notebook | Description |
|----------|-------------|
| `knn_imputation.ipynb` | Imputation des valeurs manquantes |
| `clustering_kmeans.ipynb` | Elbow method + KMeans (k=6) |
| `WS_Exploratory_Data_Analysis_Etudiant.ipynb` | Analyse exploratoire (EDA) |

## Fichiers

| Fichier | Description |
|---------|-------------|
| `data/housing.csv` | Dataset original |
| `data/housing_data_knn.csv` | Dataset imputé (0 NaN) |
| `data/housing_data_knn_clustered.csv` | Dataset avec colonne `cluster` |
| `rapport_clustering.pdf` | Rapport |

## Ressources

- [KMeans Clustering Algorithm (SlideShare)](https://www.slideshare.net/slideshow/kmeans-clustering-algorithmpptx/260166253)
- [Elbow Method (Built In)](https://builtin.com/data-science/elbow-method)
- [Standard Score (Wikipedia)](https://en.wikipedia.org/wiki/Standard_score)
- [K-means Clustering (Wikipedia)](https://en.wikipedia.org/wiki/K-means_clustering)
