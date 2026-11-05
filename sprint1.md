Voici le récapitulatif des étapes réalisées dans le **Sprint 1 — Collecte, exploration et nettoyage du corpus COFI**.

### Sprint 1 — Collecte, exploration et nettoyage du corpus

| N° | Étape | Travail à réaliser | État |
|---|---|---|---|
| 1.1 | Identification des sources de données | Identifier les sources de données disponibles pour constituer le corpus COFI | ✅ |
| 1.2 | Collecte du corpus Hugging Face | Télécharger le sous-ensemble français de `multilingual-gec` | ✅ |
| 1.3 | Collecte des données synthétiques | Constituer deux corpus supplémentaires de 100 et 5 000 paires générées avec Claude | ✅ |
| 1.4 | Organisation des données brutes | Stocker les fichiers originaux dans `data/raw/` | ✅ |
| 1.5 | Exploration du corpus Hugging Face | Examiner les colonnes, les dimensions, les valeurs manquantes et les longueurs des phrases | ✅ |
| 1.6 | Nettoyage du corpus Hugging Face | Supprimer le préfixe `fix grammar:`, harmoniser les espaces et éliminer les paires vides, identiques et les doublons | ✅ |
| 1.7 | Vérification des corpus Claude | Contrôler les dimensions, les valeurs manquantes, les paires identiques et les doublons | ✅ |
| 1.8 | Harmonisation des sources | Uniformiser les colonnes, normaliser les textes en Unicode NFC et ajouter les étiquettes de provenance | ✅ |
| 1.9 | Fusion des corpus | Regrouper les trois sources dans un corpus unifié | ✅ |
| 1.10 | Vérification du corpus unifié | Contrôler les dimensions, les doublons, les paires identiques et les valeurs manquantes | ✅ |
| 1.11 | Inspection qualitative | Examiner des exemples de chaque source pour évaluer la cohérence des corrections | ✅ |
| 1.12 | Détection des troncatures | Concevoir et améliorer une méthode de détection des phrases structurellement incomplètes | ✅ |
| 1.13 | Identification des paires suspectes | Repérer les paires contenant des indices de troncature | ✅ |
| 1.14 | Constitution du corpus final | Exclure les 3 810 paires suspectes et conserver les 67 063 paires restantes | ✅ |
| 1.15 | Vérification du corpus final | Contrôler les dimensions, les doublons, les paires identiques et les valeurs manquantes | ✅ |
| 1.16 | Sauvegarde du corpus final | Enregistrer le corpus final en CSV et Parquet dans `data/processed/` | ✅ |

### Bilan du Sprint 1

| Indicateur | Résultat |
|---|---:|
| Paires Hugging Face initiales | 66 500 |
| Paires Claude | 5 100 |
| Total après fusion | 70 873 |
| Paires suspectes exclues | 3 810 |
| **Corpus final** | **67 063** |

**Répartition du corpus final :**

- Hugging Face : 61 963 paires.
- Claude 5000 : 5 000 paires.
- Claude 100 : 100 paires.

### Statut du Sprint 1 : ✅ TERMINÉ

**Remarque méthodologique :** les trois sources sont synthétiques. Le corpus ne doit donc pas être présenté comme un ensemble de corrections collectées directement auprès de véritables apprenants.

Nous disposons maintenant d'une base de données harmonisée et documentée pour poursuivre le développement de COFI.