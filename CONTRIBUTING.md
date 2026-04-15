# 🤝 Guide de Contribution M-CORE

Merci de l'intérêt que vous portez à **M-CORE** ! Pour maintenir une qualité industrielle et une portabilité universelle, nous appliquons des standards rigoureux. En contribuant, vous acceptez de respecter ce protocole.

---

## 🚦 Avant de commencer

1. **Vérifiez les Issues :** Assurez-vous qu'une issue existe pour votre modification.
2. **Discutez d'abord :** Pour des changements majeurs, ouvrez une [Discussion](https://github.com/orgs/M-Core-Engineering/discussions) avant de coder.

---

## 🛠️ Workflow de Développement

### 1. Préparation de l'environnement

Nous utilisons `Go-Task` pour garantir la cohérence entre OS.

```bash
git clone --recursive https://github.com/orgs/M-Core-Engineering/m-core
cd m-core
task init
task setup
```

## 2. Cycle de Branchement

Nous suivons un modèle **GitFlow Hybride** :

* Toute nouvelle fonctionnalité doit partir d'une branche **`feat/nom-de-la-feature`**.
* Toute correction de bug doit partir d'une branche **`fix/nom-du-bug`**.
* Les branches de développement sont fusionnées dans **`drift`** (intégration) avant de rejoindre **`main`**.

---

## 📜 Standards de Code & Documentation

## 1. Qualité du Code

* **Linting** : Votre code doit passer **`task check`** sans avertissement.
* **Documentation** : Tout nouveau module doit être documenté dans le dossier **docs/** et mis à jour dans le **README.md** concerné.
* **M-SPEC** : Pour la documentation, respectez strictement le frontmatter YAML et les chemins relatifs.

## 2. Convention de Commit

Nous utilisons la norme Conventional Commits :

* **`feat`**: pour une nouvelle fonctionnalité.
* **`fix`**: pour une correction.
* **`docs`**: pour des changements de documentation.
* **`chore`**: pour la maintenance (ex: mise à jour du Taskfile).

---

## ✅ Definition of Done (DoD)

Avant de soumettre votre **Pull Request**, cochez cette liste :

* [ ]  **`task check`** (Linters) passe avec succès.
* [ ]  Les **tests unitaires** sont au vert.
* [ ]  La **documentation** a été mise à jour.
* [ ]  Le **message de commit** est explicite et suit la norme.
* [ ]  L'**issue** associée est référencée (ex: Closes #12).

---

## 🔐 Sécurité

* Ne soumettez jamais de fichiers **`.env`** ou de **secrets**.
* Les **PRs** contenant des secrets seront immédiatement fermées et les commits réécrits.

---

© 2024 M-CORE Engineering - Bâtir des outils résilients, partout, pour tous.
