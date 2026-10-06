# ai-toolkit

> Reusable prompt modes and skills for AI assistants, maintained by 9 Lives IT Solutions.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

[Version française](README.fr.md)

---

## Overview

This repository collects Markdown files that can be loaded into an AI assistant: prompt modes that change how the assistant works on a task, and skills that give it a method for a specific technical domain. Each file is standalone and starts with a YAML front matter (`name`, `description`) that tells the assistant when to use it.

Content is written in French.

---

## Contents

| File | Type | Purpose |
| ---- | ---- | ------- |
| `providers/anthropic/prompts/modes/planification.md` | Prompt mode | Planning mode: no final content is produced, the assistant only analyses and clarifies the project with multiple-choice questions |
| `skills/infrastructure/ldap-nodejs.md` | Skill | LDAP / Active Directory integration in a Node.js/Express application (authentication, group-based roles, configuration wizard, troubleshooting) |

---

## Usage

Copy the file you need into the configuration of your assistant (custom instructions, project knowledge or skills folder, depending on the tool). The `description` field in the front matter states the trigger conditions.

---

## Project Structure

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

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'feat: add my-feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

Please follow [Conventional Commits](https://www.conventionalcommits.org/) for commit messages.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Maintained by **9 Lives IT Solutions** — Healthcare IT & Infrastructure Automation.
