# ai-toolkit

> Modes de prompt et skills réutilisables pour assistants IA, maintenus par 9 Lives IT Solutions.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

[English version](README.md)

---

## Présentation

Ce dépôt rassemble des fichiers Markdown à charger dans un assistant IA : des modes de prompt qui changent la façon dont l'assistant travaille sur une tâche, et des skills qui lui donnent une méthode pour un domaine technique précis. Chaque fichier est autonome et commence par un en-tête YAML (`name`, `description`) qui indique à l'assistant quand l'utiliser.

Le contenu est rédigé en français.

---

## Contenu

| Fichier | Type | Rôle |
| ------- | ---- | ---- |
| `providers/anthropic/prompts/modes/planification.md` | Mode de prompt | Mode planification : aucun contenu final n'est produit, l'assistant analyse et clarifie le projet avec des questions à choix |
| `skills/infrastructure/ldap-nodejs.md` | Skill | Intégration LDAP / Active Directory dans une application Node.js/Express (authentification, rôles par groupes, assistant de configuration, dépannage) |

---

## Utilisation

Copier le fichier voulu dans la configuration de votre assistant (instructions personnalisées, connaissances de projet ou dossier de skills, selon l'outil). Le champ `description` de l'en-tête précise les conditions de déclenchement.

---

## Structure du projet

```
ai-toolkit/
├── providers/
│   └── anthropic/
│       └── prompts/
│           └── modes/
│               └── planification.md
├── skills/
│   └── infrastructure/
│       └── ldap-nodejs.md
├── README.md
├── README.fr.md
└── LICENSE
```

---

## Contribuer

1. Forker le dépôt
2. Créer une branche (`git checkout -b feature/ma-fonctionnalite`)
3. Commiter (`git commit -m 'feat: add ma-fonctionnalite'`)
4. Pousser la branche (`git push origin feature/ma-fonctionnalite`)
5. Ouvrir une Pull Request

Merci de suivre les [Conventional Commits](https://www.conventionalcommits.org/) pour les messages de commit.

---

## Licence

Ce projet est distribué sous licence MIT. Voir le fichier [LICENSE](LICENSE).

---

Maintenu par **9 Lives IT Solutions** — Informatique de santé & automatisation d'infrastructure.
