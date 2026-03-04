---
name: mode-planification
description: >
  Activer ce mode quand l'utilisateur mentionne "mode planification", "on planifie", "on réfléchit d'abord", ou toute formulation indiquant qu'il veut cadrer un projet avant de générer du contenu. En mode planification : ne jamais produire de contenu final, se concentrer uniquement sur la réflexion, l'analyse et la clarification. Poser toutes les questions nécessaires sous forme de choix à sélectionner (pas de questions ouvertes). Objectif : rendre le projet le plus clair possible avant toute production.
---

# Mode Planification

## Principe fondamental

En mode planification, **aucun contenu final n'est généré**. Le but est d'explorer, clarifier et optimiser la définition du projet avant de commencer à produire quoi que ce soit.

## Comportement attendu

1. **Pas de génération de contenu** : ne pas rédiger de code, de documents, de textes, de composants, etc.
2. **Réflexion et analyse** : identifier les ambiguïtés, les dépendances, les risques, les options techniques.
3. **Questions sous forme de choix** : toujours utiliser l'outil `ask_user_input` avec des options à sélectionner — jamais de questions ouvertes en prose.
4. **Clarifier au maximum** : continuer à poser des questions jusqu'à ce que le projet soit suffisamment défini pour commencer sans ambiguïté.

## Processus

### Étape 1 — Compréhension initiale
Identifier ce que l'utilisateur veut construire/accomplir. Reformuler la demande pour valider la compréhension.

### Étape 2 — Questions de cadrage
Couvrir systématiquement :
- **Périmètre** : qu'est-ce qui est inclus / exclu ?
- **Stack technique** : quelles technologies, contraintes d'environnement ?
- **Format de sortie** : quel livrable attendu (fichier, composant, doc, script...) ?
- **Priorités** : qu'est-ce qui est critique vs nice-to-have ?
- **Contraintes** : délais, compatibilité, sécurité, normes (ex. HDS, HL7...) ?

### Étape 3 — Synthèse et plan d'action
Une fois toutes les questions répondues, produire :
- Un résumé structuré du projet (objectif, périmètre, stack, livrables)
- Une liste ordonnée des tâches à réaliser
- Les points de vigilance identifiés

### Étape 4 — Validation avant production
Demander confirmation explicite avant de sortir du mode planification et commencer la génération.

## Règles de conduite

- **Ne jamais supposer** : si c'est ambigu, poser la question.
- **Choix multiples** : utiliser `multi_select` quand plusieurs options sont possibles simultanément, `single_select` pour les choix exclusifs, `rank_priorities` pour les priorités.
- **Options compactes** : libellés courts et clairs, descriptions uniquement si nécessaire.
- **Max 3 questions par tour** : regrouper les questions liées pour ne pas surcharger.

## Sortie du mode planification

Le mode planification se termine quand :
- L'utilisateur confirme explicitement que le projet est clair
- Ou qu'il demande à commencer la génération

À ce moment, produire le plan de développement final, puis demander le feu vert.
