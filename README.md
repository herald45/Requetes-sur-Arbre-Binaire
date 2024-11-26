# Projet de Programmation Fonctionnelle : Structure de Données pour Requêtes sur Arbre Binaire

## Description

Ce projet consiste à implémenter une structure de données basée sur un arbre binaire pour effectuer des requêtes sur un tableau d'entiers. La structure doit permettre :

1. **Créer** une représentation de l'arbre à partir d'une liste d'entiers.
2. **Mettre à jour** une valeur dans le tableau et propager les modifications dans l'arbre.
3. **Effectuer des requêtes** spécifiques sur des intervalles du tableau.

Les types de requêtes possibles incluent :
- **Somme des éléments** d’un intervalle.
- **Valeur maximum et son nombre d’occurrences** dans un intervalle.
- **Plus grande somme d’un sous-tableau contigu** dans un intervalle.

Le projet utilise l’outil **Dune** pour la gestion des modules et des tests.


## Installation et Compilation

1. **Prérequis** : 
   - OCaml installé sur votre machine.
   - Outil Dune installé (version recommandée : ≥ 2.9.0).

2. **Compilation** : 
   - Clonez le projet ou téléchargez l'archive.
   - Placez-vous dans le dossier du projet.
   - Exécutez la commande suivante pour compiler :
     ```bash
     dune build
     ```

3. **Tests** :
   - Exécutez les tests pour vérifier votre implémentation :
     ```bash
     dune runtest
     ```

---

## Usage

Les trois modules principaux doivent respecter les signatures fournies. Voici un aperçu de leur utilisation :

### Création d’un Arbre

Pour initialiser un arbre binaire à partir d’une liste d’entiers :
```ocaml
let tree = QueryStructure.create [1; -4; 6; 8]
```

### Mise à jour d’un élément

Pour mettre à jour la valeur d’un élément dans le tableau et modifier la structure :
```ocaml
let updated_tree = QueryStructure.update tree 10 2  (* Met à jour l'élément à l'indice 2 *)
```

### Requêtes

Pour effectuer une requête (par exemple, calculer la somme des éléments dans un intervalle) :
```ocaml
let result = QueryStructure.query tree 1 3  (* Requête pour l'intervalle [1...3] *)
```

Chaque module gère des types spécifiques de requêtes :
- `NodeSum` pour la somme.
- `NodeMaxOcc` pour le maximum et les occurrences.
- `NodeMaxSubseg` pour la plus grande somme contiguë.

---

## Notes Importantes

- Le nombre d'éléments dans le tableau doit toujours être une puissance de 2.
- Ne modifiez pas les fichiers fournis, sauf les fichiers de module (`node_sum.ml`, `node_max_occ.ml`, etc.).
- Respectez strictement les noms des fichiers et des fonctions pour éviter les erreurs dans les tests.

---

## Licence

Ce projet est destiné à un usage pédagogique. Toute reproduction ou distribution sans autorisation est interdite.

---
