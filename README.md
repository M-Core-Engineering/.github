# 🛡️ M-CORE Engineering | Governance & Standards

**Le socle de rigueur industrielle pour l'écosystème M-CORE.**  
*Opérationnalisation des processus, standards de qualité et protocoles SDLC.*

---

## 📖 Sommaire

- [🛡️ M-CORE Engineering | Governance \& Standards](#️-m-core-engineering--governance--standards)
  - [📖 Sommaire](#-sommaire)
  - [🎯 Vision \& Éthique](#-vision--éthique)
  - [⚖️ Stratégie de l'Écosystème (Meta-Sourcing)](#️-stratégie-de-lécosystème-meta-sourcing)
  - [🛠️ Protocole de Développement (SDLC)](#️-protocole-de-développement-sdlc)
    - [1. Stratégie de Branchement \& Versioning](#1-stratégie-de-branchement--versioning)
    - [2. Definition of Done (DoD)](#2-definition-of-done-dod)
  - [🔐 Sécurité \& Intégrité](#-sécurité--intégrité)
  - [🌍 Communication \& Onboarding](#-communication--onboarding)
  - [🔗 Liens de Gouvernance](#-liens-de-gouvernance)

---

## 🎯 Vision & Éthique

M-CORE normalise la production technique de haute fidélité en mode **Offline-First**. Nous considérons la documentation et l'automatisation comme des actifs de production au même titre que le code source.

> **Règle d'Or :** Tout ce qui n'est pas automatisé ou documenté n'existe pas.

---

## ⚖️ Stratégie de l'Écosystème (Meta-Sourcing)

Nous appliquons une séparation stricte des préoccupations (SoC) par dépôt pour garantir la modularité et la sécurité de l'infrastructure :

| Dépôt | Rôle Stratégique | Essence | Visibilité |
| --- | --- | --- | --- |
| m-core | Orchestrateur & Entry-point | Principal | [PUBLIC] |
| .task | Automation Logic (CI/CD Locale) | Core Tooling | [PUBLIC] |
| .github | Gouvernance & SDLC | Profile | [PUBLIC] |
| spec | Schémas de données & Contrats | Governance | [PUBLIC] |
| engine | Logique métier (Go/Rust) | Core Engine | [PRIVATE] |
| doc | Business Intelligence & Stratégie | Documentation | [PRIVATE] |
| mobile | Portabilité & Agilité | Application | [PRIVATE] |m  
| templates | Design & Présentation | Template | [PRIVATE] |
| showcase | Vitrine & Espace de publication | Espace Web | [PRIVATE] |

---

## 🛠️ Protocole de Développement (SDLC)

### 1. Stratégie de Branchement & Versioning

* **Branches :** Workflow `main` (stable) < `drift` (intégration) < `feat/` (développement).
* **Versioning :** Application stricte du [Semantic Versioning (SemVer)](https://semver.org).
* **Commits :** Respect impératif de la spécification [Conventional Commits](https://conventionalcommits.org).
  
### 2. Definition of Done (DoD)

Une PR ne peut être fusionnée que si :

* `task check` est validé (Linting & Static Analysis).
* Les **tests unitaires** (si applicables) sont au vert.
* La documentation (`/docs`) a été mise à jour.
* Le "**Sign-off**" d'au moins un **Code Owner** est obtenu.

---

## 🔐 Sécurité & Intégrité

* **Secret Scanning :** `Gitleaks` est activé sur l'organisation. Tout secret détecté entraîne l'invalidation immédiate de la PR.
* **Dependency Management :** Priorité aux dépendances statiques. Toute nouvelle dépendance doit être justifiée dans la PR.
* **Audit :** Les logs de déploiement sont immuables et liés à l'empreinte Git (commit SHA).

---

## 🌍 Communication & Onboarding

* **Questions :** Utilisez l'onglet [Discussions](https://github.com) pour les questions non techniques.
* **Bugs :** Ouvrez une [Issue](https://github.com) avec le template dédié.
* **Code of Conduct :** Nous appliquons le [Contributor Covenant](https://contributor-covenant.org).

---

## 🔗 Liens de Gouvernance

* [Guide de Contribution complet](./CONTRIBUTING.md)
* [Politique de Sécurité (Vulnerability Disclosure)](./SECURITY.md)
* [Templates d'Organisation](./workflow-templates)

---

© 2024 **M-CORE Engineering** - *L'ingénierie résiliente au service de la continuité.*