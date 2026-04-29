# **Classification des Tumeurs Mammaires par Arbres de Décision**

## Contexte du Projet
J'ai réalisé ce projet dans le cadre d'un TP Data Mining et Machine Learning. Il simule une mission pour l'entreprise **MedTech Solutions**, qui cherche à développer une solution d'intelligence artificielle pour assister le diagnostic médical d'un centre hospitalier. 

L'objectif initial était de réduire le taux d'erreur de diagnostic (initialement à 20 %) lors de la classification des tumeurs mammaires (malignes ou bénignes), en utilisant un modèle interprétable.

## Données
Le jeu de données utilisé est le **Breast Cancer Wisconsin Dataset**, directement disponible via la librairie `scikit-learn`.
* **Observations :** 569 patientes
* **Variables explicatives :** 30 caractéristiques numériques calculées à partir d'images numérisées d'une ponction à l'aiguille fine (FNA) d'une masse mammaire (rayon, texture, périmètre, etc.).
* **Variable cible :** `target` (0 = Maligne, 1 = Bénigne).

## Modélisation et Résultats
Nous avons testé et comparé plusieurs modèles d'Arbres de Décision (`DecisionTreeClassifier`) qui sont:
1. Arbre avec critère de **Gini** (profondeur max = 3)
2. Arbre avec critère d'**Entropie** (profondeur max = 3) - qui sera par la suite le **Modèle retenu**
3. Arbre sans contrainte de profondeur qui a été une mise en évidence du surapprentissage

**Performances du modèle final (Entropie, max_depth=3) sur l'ensemble de test :**
* **Accuracy globale :** ~ 95 %
* **Recall (Sensibilité) pour la classe Maligne :** ~ 90 %
* **AUC-ROC :** 0.945
* **Bilan métier :** Le taux d'erreur global a été abaissé à environ 5 %, remplissant largement l'objectif de réduction des 20 % d'erreurs historiques du client. Le modèle agit comme un excellent outil de "second avis clinique".

## Comment exécuter ce projet ?

### Prérequis
Assurez-vous d'avoir Python installé ainsi que les librairies suivantes :
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
Vous pouvez également utilisez Google Colab https://colab.research.google.com

Bonne exploration.
