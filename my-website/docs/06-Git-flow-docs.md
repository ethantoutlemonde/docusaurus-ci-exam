
---

### **README - Git Flow**  

```md
# 🌱 Git Flow - Organisation du Développement

Git Flow est une méthodologie de gestion de branches qui permet un **développement structuré** et une **collaboration efficace**.

---

## 📌 1️⃣ Branches Principales

- **`main`** : Contient le code **stable** en production.
- **`DocsRedac`** : Intègre les **nouvelles fonctionnalités** avant d’être fusionné dans `main`.

---

## 📌 2️⃣ Branches Secondaires

- **`feature/nom-de-la-feature`** : Pour **chaque nouvelle fonctionnalité**.
- **`release/nom-de-la-release`** : Pour **préparer une version stable** avant production.
- **`hotfix/nom-du-hotfix`** : Pour **corriger un bug en production** rapidement.

---

## 📌 3️⃣ Workflow Typique

### **1️⃣ Créer une nouvelle fonctionnalité**

```sh
git checkout DocsRedac
git pull origin DocsRedac
git checkout -b feature/nouvelle-fonctionnalité
