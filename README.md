# 🛡️ M-CORE Engineering | Governance & Standards

**Le socle de rigueur industrielle pour l'écosystème M-CORE.** *Définition des processus, standards de qualité et protocoles de cycle de vie (SDLC).*

-----

## 🎯 Vision & Mission

**M-CORE** (Mobile-first Continuity & Offline Rendering Engine) brise la dépendance aux infrastructures fixes. Nous transformons la contrainte (instabilité énergétique/réseau) en opportunité technologique en normalisant la production technique de haute fidélité en mode **Offline-First**.

> **Note aux contributeurs :** L'adhésion aux standards définis ici n'est pas optionnelle. Elle garantit la portabilité universelle (ARM64/x86\_64) et la pérennité du savoir.

-----

## ⚖️ Stratégie de l'Écosystème

### 1\. Architecture des Dépôts (Meta-Sourcing)

L'écosystème est segmenté en unités fonctionnelles pour maximiser la maintenance :

| Dépôt | Rôle | Essence |
| :--- | :--- | :--- |
| **`m-core`** | **Conteneur Parent** | Orchestration globale et point d'entrée unique. |
| **`spec`** | **Source de Vérité** | Règles YAML, schémas de validation et d'édition. |
| **`engine`** | **Noyau de Rendu** | Logique de transformation haute performance (Rust/Go). |
| **`workspace`** | **Zone de Production** | Contenu métier, notes techniques et assets. |
| **`.github`** | **Gouvernance** | Profil d'organisation, Workflows partagés et SDLC. |

### 2\. Standard d'Édition : M-SPEC

Pour garantir un rendu cross-plateforme sans erreur, chaque fichier `.md` doit respecter :

* **Frontmatter YAML strict** (Validation via `markdownlint-cli2`).
* **Encodage UTF-8 sans BOM**.
* **Chemins relatifs uniquement** (Interdiction des chemins absolus pour la portabilité Android/Linux/Windows).

-----

## 🛠️ Protocole de Développement (SDLC)

### 1\. Workflow de Contribution

Nous appliquons un **GitFlow Hybride** rigoureux :

1. **Branche `feat/` ou `fix/`** : Développement isolé.
2. **Pull Request (PR)** : Déclenchement automatique des tests de linting (`Vale`, `Markdownlint`).
3. **Branche `drift`** : Zone d'intégration continue (Pré-production).
4. **Branche `main`** : Production stable. **Protection de branche activée (Push direct interdit).**

### 2\. Standards de Qualité (Definition of Done)

Une tâche est considérée comme "Terminée" uniquement si :

* [ ] Le code/document passe le linter local (`task check`).
* [ ] Les messages de commit suivent la convention **Conventional Commits**.
* [ ] La documentation associée a été mise à jour simultanément.
* [ ] Le rendu PDF (Typst) et Web (Zola) est exempt d'artefacts visuels.

-----

## 🔐 Sécurité & Conformité

* **Zéro Secret** : Utilisation obligatoire de `.env.example` et scan `Gitleaks` en pré-commit.
* **Auditabilité** : Chaque déploiement sur Cloudflare Pages doit être lié à un SHA de commit vérifié.
* **Indépendance logicielle** : Priorité aux binaires statiques pour éviter les vecteurs d'attaque par dépendances dynamiques.

-----

## 🌍 Accessibilité & Marketing Technique

M-CORE n'est pas seulement un outil, c'est un produit. Nos livrables (PDF/Web) sont conçus pour être monétisables auprès d'entreprises locales et d'entités éducatives, grâce à une mise en page de précision industrielle.

-----

## 🔗 Liens Utiles

* 🏠 **[Page d'accueil M-CORE](https://github.com/M-Core-Engineering/m-core)** : Point d'entrée technique et installation.
* 📚 **[Documentation Spécifique](https://github.com/M-Core-Engineering/spec)** : Détails des grammaires de validation.
