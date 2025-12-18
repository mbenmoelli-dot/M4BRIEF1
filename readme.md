\# 📘 Benchmark de modèles d’IA pour une tâche de régression  

\*\*Prédiction des prix de l’immobilier – Dataset Boston\*\*



\## 1. Contexte du projet



Ce projet s’inscrit dans le cadre du \*\*Module M4 – Concevoir une IA simple (FastIA)\*\*,  

Brief 1 : \*Benchmark de modèles d’IA pour une tâche de régression\*.



FastIA souhaite développer un \*\*modèle de prédiction des prix de l’immobilier\*\* à partir de données historiques issues de la ville de Boston.  

L’objectif est d’aider des acteurs publics et privés à \*\*estimer la valeur de logements\*\* dans une logique d’aide à la décision.



Le projet adopte une \*\*démarche scientifique rigoureuse\*\* :

\- formulation d’hypothèses,

\- expérimentation de plusieurs modèles,

\- évaluation comparative,

\- interprétation des résultats,

tout en intégrant les \*\*enjeux métiers, éthiques et techniques\*\*.



---



\## 2. Objectifs du projet



Les objectifs principaux sont :



\- Nettoyer et préparer un dataset de données réelles

\- Construire un pipeline de preprocessing reproductible

\- Tester plusieurs modèles de régression

\- Comparer leurs performances à l’aide de métriques adaptées

\- Analyser les résultats et identifier les limites des modèles

\- Intégrer une réflexion éthique sur l’usage des données



---



\## 3. Dataset utilisé



\### Dataset immobilier de Boston



Le dataset contient des informations \*\*socio-économiques et urbaines\*\* influençant les prix de l’immobilier.



Exemples de variables :

\- caractéristiques des logements,

\- environnement urbain,

\- indicateurs socio-économiques,

\- accessibilité et infrastructures.



\### Variable cible

\- \*\*Prix médian des logements\*\* (variable continue)



\### Particularités du dataset

\- Présence de valeurs manquantes potentielles

\- Outliers possibles

\- Variables hétérogènes (échelles différentes)

\- Données sensibles d’un point de vue éthique (risque de biais sociaux)



---



\## 4. Analyse éthique et métier



Une attention particulière est portée à :



\- la \*\*représentativité des données\*\*

\- le risque de \*\*biais socio-économiques\*\*

\- l’usage responsable des prédictions

\- les limites d’un modèle entraîné sur des données historiques



Le modèle ne doit pas être interprété comme une vérité absolue, mais comme \*\*un outil d’aide à la décision\*\*.



---



\## 5. Pipeline de préparation des données



Un pipeline robuste et reproductible est mis en place, comprenant :



\- Gestion des valeurs manquantes (NaN)

\- Traitement des outliers

\- Encodage des variables catégorielles (si présentes)

\- Normalisation / standardisation des variables numériques

\- Séparation train / test

\- Validation croisée



Ces étapes garantissent :

\- la cohérence des données,

\- l’équité de comparaison entre modèles,

\- l’absence de fuite de données.



---



\## 6. Modèles de régression testés



Les modèles suivants ont été implémentés et comparés :



\### 🔹 Régression Linéaire

\- Modèle simple et interprétable

\- Sert de \*\*baseline\*\*

\- Sensible aux relations linéaires et aux outliers



\### 🔹 Random Forest Regressor

\- Modèle non linéaire basé sur des arbres de décision

\- Bonne gestion des interactions complexes

\- Robuste au bruit et aux outliers



\### 🔹 LightGBM Regressor

\- Modèle de gradient boosting optimisé

\- Très performant sur données tabulaires

\- Entraînement rapide et efficace

\- Sensible au réglage des hyperparamètres



---



\## 7. Méthodologie d’évaluation



Les performances des modèles sont évaluées à l’aide de :



\- \*\*RMSE\*\* (Root Mean Squared Error)

\- \*\*MAE\*\* (Mean Absolute Error)

\- \*\*R²\*\* (coefficient de détermination)

\- \*\*Validation croisée\*\* pour garantir la robustesse des résultats



Les métriques sont comparées sur les mêmes splits afin d’assurer une comparaison équitable.



---



\## 8. Résultats et comparaison



\### Tendances observées



\- La régression linéaire fournit une baseline correcte mais limitée

\- Random Forest améliore nettement la performance

\- LightGBM offre généralement les meilleurs résultats en termes de précision



\### Analyse comparative



| Modèle | Performance | Interprétabilité | Complexité |

|------|-------------|------------------|------------|

| Régression linéaire | Moyenne | Élevée | Faible |

| Random Forest | Élevée | Moyenne | Moyenne |

| LightGBM | Très élevée | Faible | Élevée |



---



\## 9. Analyse des limites



\- Dépendance à la qualité des données historiques

\- Risque de biais socio-économiques

\- Interprétabilité réduite des modèles complexes

\- Généralisation limitée à des contextes similaires à Boston



---



\## 10. Livrables



\- ✅ Notebook Jupyter documenté (code, graphiques, interprétations)

\- ✅ Pipeline de préparation des données reproductible

\- ✅ Benchmark de modèles de régression

\- ✅ Analyse critique des résultats



\### Bonus (optionnels)

\- API FastAPI exposant le modèle

\- Suivi des expériences avec MLflow

\- Conteneurisation avec Docker



---



\## 11. Conclusion



Ce projet démontre l’importance d’un \*\*benchmark rigoureux\*\* dans le choix d’un modèle de régression.



Si les modèles avancés offrent de meilleures performances, leur utilisation doit être mise en balance avec :

\- la complexité,

\- l’interprétabilité,

\- les contraintes métiers et éthiques.



Dans une logique d’aide à la décision, le modèle retenu doit être \*\*fiable, explicable et responsable\*\*.



