# 🛡️ M-Core Engineering | Governance & Standards

Bienvenue dans l'organisation **M-Core Engineering**. Ce dépôt centralise les standards, les règles de gouvernance et les processus de cycle de vie (SDLC) applicables à l'ensemble de l'écosystème M-CORE.

## 🎯 Vision & Mission

**M-CORE** (Mobile-first Continuity & Offline Rendering Engine) a pour mission de briser la dépendance aux infrastructures fixes en permettant une production technique de haute qualité (Docs-as-Code) en conditions de mobilité et de réseau instables.

---

## ⚖️ Gouvernance de l'Organisation

### 1. Structure des Dépôts

Chaque dépôt de l'organisation a un rôle spécifique pour garantir la modularité :

* **`spec`** : Standard d'édition et règles de validation (Source de vérité).
* **`engine`** : Cœur de rendu haute performance (Rust/Go).
* **`templates`** : Catalogue de thèmes industriels (Zola/Typst).
* **`mobile`** : Interfaces clients et PWA.
* **`showcase`** : Vitrine des déploiements et démonstrations commerciales.

### 2. Stratégie de Branchement (GitFlow Hybride)

Pour garantir la stabilité de la production (`main`), nous appliquons strictement le flux suivant :

* **`feat/`**, **`fix/`**, **`docs/`** : Branches éphémères pour le développement.
* **`drift`** : Branche d'intégration et de pré-production (Zone de test).
* **`main`** : Branche de production verrouillée. **Le push direct est proscrit.**

---

## 🛠️ Standards de Qualité (M-CORE STD)

Tout dépôt au sein de cette organisation doit se conformer aux exigences suivantes :

| Domaine | Outil de Validation | Standard |
| :--- | :--- | :--- |
| **Structure Markdown** | `markdownlint-cli2` | Conformité aux règles `.markdownlint.yaml` du repo `spec`. |
| **Style & Sémantique** | `Vale` | Ton pédagogique et professionnel conforme au guide de style. |
| **Intégrité** | `Lychee` | Zéro lien mort (Broken Links) toléré. |
| **Typographie** | `Typst` | Rendu PDF de précision mathématique et industrielle. |

---

## 🤝 Contribution & Éthique

L'ingénierie chez M-Core repose sur le passage de "l'artisanat à la rigueur".

1. **Qualité par Design** : On ne code pas pour que "ça marche", on code pour que ce soit maintenable.
2. **Documentation as Code** : La documentation est produite en même temps que le code, jamais après.
3. **Conventional Commits** : Les messages de commit doivent suivre la norme (ex: `feat: add new typst template`).

---

## 📜 Licence

Sauf mention contraire explicite dans un dépôt spécifique, l'ensemble des travaux de l'organisation **M-Core Engineering** est distribué sous la licence **Apache-2.0**.

---
*Fait avec rigueur à Dschang, 2026.*
