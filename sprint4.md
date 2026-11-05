Parfait ! Nous passons au **Sprint 4 — Entraînement du modèle COFI**. C'est une étape majeure : nous allons apprendre au modèle à transformer une phrase incorrecte en phrase correcte à partir de notre corpus préparé.

Nous allons conserver notre méthode de travail : **une étape à la fois, une cellule de code à la fois**. Tu exécutes la cellule, tu me transmets le résultat, puis nous vérifions avant de continuer.

## Objectifs du Sprint 4

Voici les travaux que nous allons réaliser :

| N° | Étape | Travail à réaliser | État |
| :--- | :--- | :--- | :---: |
| 4.1 | Préparation des poids de masquage | Créer les poids permettant d'ignorer les tokens `<PAD>` pendant l'entraînement et la validation | ⏳ |
| 4.2 | Vérification des données d'entraînement | Contrôler les dimensions, les types et les poids des séquences | ⏳ |
| 4.3 | Définition des hyperparamètres | Choisir la taille des lots (*batch size*), le nombre d'époques et les paramètres d'entraînement | ⏳ |
| 4.4 | Configuration des callbacks | Préparer l'arrêt anticipé et la sauvegarde du meilleur modèle | ⏳ |
| 4.5 | Préparation de l'entraînement | Vérifier les entrées, les cibles et les poids transmis à Keras | ⏳ |
| 4.6 | Entraînement du modèle | Lancer l'apprentissage sur les données d'entraînement | ⏳ |
| 4.7 | Suivi de l'apprentissage | Examiner la perte d'entraînement et la perte de validation à chaque époque | ⏳ |
| 4.8 | Gestion du meilleur modèle | Conserver les poids correspondant aux meilleures performances de validation | ⏳ |
| 4.9 | Sauvegarde du modèle entraîné | Enregistrer le modèle et son historique dans `models/` | ⏳ |
| 4.10 | Vérification des fichiers sauvegardés | Recharger les fichiers et vérifier leur intégrité | ⏳ |

**Précaution importante :** notre modèle possède plus de 20 millions de paramètres et TensorFlow a déjà signalé une consommation mémoire importante. Nous commencerons donc avec des lots de petite taille, puis nous ajusterons selon les ressources disponibles. Nous ne lancerons pas directement un entraînement massif.
