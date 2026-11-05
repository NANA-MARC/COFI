Voici le bilan détaillé du **Sprint 3 — Conception et vérification de l'architecture du modèle COFI**, présenté dans le même format que les bilans des Sprints 1 et 2.

## Sprint 3 — Conception et vérification de l'architecture du modèle

| N° | Étape | Travail à réaliser | État |
| :--- | :--- | :--- | :---: |
| 3.1 | Analyse du code du coéquipier | Examiner le notebook du coéquipier afin de comprendre l'architecture proposée et les différentes étapes de construction du modèle | ✅ |
| 3.2 | Adaptation aux données COFI | Adapter les paramètres du modèle aux dimensions et aux caractéristiques des données préparées pendant le Sprint 2 | ✅ |
| 3.3 | Chargement des paramètres | Charger les paramètres de préparation depuis `parametres_preparation.json` | ✅ |
| 3.4 | Définition des paramètres du modèle | Définir la taille du vocabulaire, les longueurs des séquences, la dimension des embeddings et le nombre d'unités LSTM | ✅ |
| 3.5 | Chargement des données préparées | Charger les tableaux NumPy des ensembles d'entraînement, de validation et de test depuis les fichiers NPZ | ✅ |
| 3.6 | Construction de l'encodeur | Créer la couche Embedding et le LSTM encodeur pour transformer la phrase incorrecte en états cachés | ✅ |
| 3.7 | Construction du décodeur | Créer la couche Embedding et le LSTM décodeur initialisé avec les états de l'encodeur | ✅ |
| 3.8 | Construction de la couche de sortie | Ajouter une couche Dense avec Softmax pour prédire les probabilités des tokens du vocabulaire | ✅ |
| 3.9 | Assemblage du modèle Seq2Seq | Relier l'encodeur, le décodeur et la couche de sortie dans un modèle unique | ✅ |
| 3.10 | Vérification de l'architecture | Examiner le résumé du modèle avec `model.summary()` et contrôler les dimensions des différentes couches | ✅ |
| 3.11 | Vérification du nombre de paramètres | Calculer manuellement le nombre de paramètres et le comparer au résultat fourni par Keras (20 346 605 paramètres) | ✅ |
| 3.12 | Vérification de l'initialisation des poids | Examiner les poids initiaux et vérifier qu'aucun poids préentraîné n'a été chargé | ✅ |
| 3.13 | Test du passage avant | Effectuer une prédiction avec des données artificielles et vérifier les dimensions de sortie ainsi que la somme des probabilités | ✅ |
| 3.14 | Compilation du modèle | Configurer l'optimiseur Adam et la fonction de perte Sparse Categorical Crossentropy | ✅ |
| 3.15 | Test initial de la fonction de perte | Effectuer une évaluation artificielle pour vérifier le fonctionnement de la compilation et de la fonction de perte | ✅ |
| 3.16 | Gestion du masquage des tokens PAD | Configurer `mean_with_sample_weight` pour exclure les positions de padding du calcul de la perte | ✅ |
| 3.17 | Vérification du masquage | Comparer la perte calculée par Keras avec une perte calculée manuellement en ignorant les tokens PAD | ✅ |
| 3.18 | Construction du modèle encodeur d'inférence | Créer un modèle indépendant permettant d'encoder une phrase incorrecte et de récupérer les états cachés | ✅ |
| 3.19 | Construction du modèle décodeur d'inférence | Créer un modèle indépendant permettant de prédire progressivement les tokens de la phrase corrigée | ✅ |
| 3.20 | Implémentation du décodage glouton | Développer la fonction `corriger_ids()` pour générer une séquence token par token jusqu'à EOS ou la longueur maximale | ✅ |
| 3.21 | Test de la génération | Vérifier le fonctionnement de la génération et l'exclusion des tokens PAD et SOS | ✅ |

### Bilan du Sprint 3

| Indicateur | Résultat |
| :--- | :--- |
| Nombre total d'étapes | 21 |
| Étapes terminées | 21 |
| Étapes restantes | 0 |
| Taille du vocabulaire | 38 125 tokens |
| Dimension des embeddings | 128 |
| Nombre d'unités LSTM | 256 |
| Nombre total de paramètres | 20 346 605 |
| Architecture | Seq2Seq avec encodeur-décodeur LSTM |
| Initialisation | Aléatoire |
| Mécanisme de génération | Décodage glouton |
| Entraînement effectué | Non |

**Statut général : SPRINT 3 TERMINÉ — 100 %.** ✅

**Remarque méthodologique :** les tests effectués jusqu'ici vérifient la construction et le fonctionnement technique de l'architecture. Ils ne démontrent pas encore sa capacité à corriger correctement le français. Cette capacité sera étudiée pendant les Sprints 4 et 5, après l'entraînement et l'évaluation du modèle.