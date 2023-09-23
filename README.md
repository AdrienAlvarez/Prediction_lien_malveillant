# Programme de Détection de Liens Malveillants

Ce dépôt contient un programme Python pour détecter les liens malveillants à l'aide d'un modèle de régression logistique.

## Description du Fichier

- `Prediction_lien_malveillant.ipynb`: Un cahier Jupyter contenant le code source du programme de détection de liens malveillants. Il comprend les étapes suivantes :
  - Importation des bibliothèques nécessaires.
  - Chargement du jeu de données depuis un fichier CSV.
  - Transformation des URL en vecteurs TF-IDF.
  - Séparation des données en ensembles d'entraînement et de test.
  - Entraînement d'un modèle de régression logistique.
  - Prédictions et évaluation de l'exactitude du modèle.
  - Sauvegarde du modèle et du vectoriseur.
  - Définition d'une fonction pour évaluer une URL en utilisant le modèle entraîné.

## Utilisation

Pour tester le programme, vous pouvez ouvrir le fichier `Prediction_lien_malveillant.ipynb` dans Google Colab (cliquez sur le lien "Open In Colab" ci-dessus). Vous pourrez ensuite exécuter le code et tester la fonction `evaluate_url()` avec un lien douteux.

## Dépendances

Assurez-vous d'avoir installé les bibliothèques Python suivantes avant d'exécuter le code :
- pandas
- scikit-learn
- joblib
- google.colab (pour l'utilisation dans Google Colab)

## Remarques

- Le modèle de régression logistique peut avertir d'une convergence limitée lors de l'entraînement. Vous pouvez ajuster les paramètres d'entraînement ou prétraiter les données pour résoudre ce problème.
- Le modèle sauvegardé et le vectoriseur sont stockés dans Google Drive.

## Exemple d'Utilisation

```python
# Vous pouvez tester la fonction en l'appelant avec un URL
url = input("Veuillez rentrer le lien douteux: ")
result = evaluate_url(url)
print(result)
