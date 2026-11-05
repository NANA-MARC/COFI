Voici le récapitulatif du **Sprint 2 — Préparation des données (Data Preprocessing)**, avec les étapes déjà réalisées et celles qu'il nous reste à effectuer, avant de poursuivre.

### Sprint 2 — Préparation des données

| N° | Étape | Travail à réaliser | État |
|---|---|---|---|
| 2.1 | Chargement du corpus final | Charger et vérifier le corpus nettoyé de 67 063 paires | ✅ |
| 2.2 | Séparation des données | Créer les ensembles train (80 %), validation (10 %) et test (10 %) | ✅ |
| 2.3 | Stratification par source | Conserver approximativement les proportions des trois sources dans chaque ensemble | ✅ |
| 2.4 | Vérification des chevauchements | Vérifier l'absence de paires exactes communes entre les trois ensembles | ✅ |
| 2.5 | Sauvegarde des ensembles | Enregistrer train, validation et test en CSV et Parquet | ✅ |
| 2.6 | Vérification des sauvegardes | Relire les fichiers et vérifier leurs dimensions et leurs colonnes | ✅ |
| 2.7 | Analyse des longueurs | Étudier les longueurs des phrases incorrectes et correctes | ✅ |
| 2.8 | Définition de la longueur maximale | Choisir une longueur maximale adaptée aux séquences | 🟡 |
| 2.9 | Normalisation des textes | Définir les règles de normalisation sans supprimer les informations linguistiques importantes | ⏳ |
| 2.10 | Tokenisation | Découper les phrases en tokens (mots et ponctuation) | ⏳ |
| 2.11 | Construction du vocabulaire | Créer un dictionnaire associant chaque token à un identifiant numérique | ⏳ |
| 2.12 | Ajout des tokens spéciaux | Ajouter `<PAD>`, `<UNK>`, `<SOS>` et `<EOS>` | ⏳ |
| 2.13 | Conversion numérique | Transformer les phrases incorrectes et correctes en séquences d'identifiants | ⏳ |
| 2.14 | Padding et troncature | Uniformiser la longueur des séquences | ⏳ |
| 2.15 | Préparation des entrées et sorties | Construire les données destinées à l'encodeur et au décodeur Seq2Seq | ⏳ |
| 2.16 | Vérification des données préparées | Contrôler les dimensions, les séquences, les tokens et les correspondances | ⏳ |
| 2.17 | Sauvegarde des artefacts | Enregistrer les vocabulaires et les données numériques préparées | ⏳ |

### Bilan actuel

- 7 étapes entièrement terminées.
- 1 étape en cours de finalisation.
- 9 étapes restantes.