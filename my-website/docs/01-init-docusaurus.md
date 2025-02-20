# 📖 Guide Complet : Déploiement de Docusaurus avec CI/CD 🚀

Ce guide explique comment configurer un site Docusaurus, le connecter à GitHub Actions pour une intégration continue (CI), le déployer sur GitHub Pages, ajouter des tests et utiliser Git Flow.

---

## 1️⃣ Initialisation du Projet Docusaurus

### 📌 Prérequis
Avant de commencer, assurez-vous d'avoir installé :
- [Node.js](https://nodejs.org/) (version 18 ou supérieure)
- [Git](https://git-scm.com/) pour le suivi des versions
- Un compte [GitHub](https://github.com/)

### 📌 Création du dossier du projet
Créez un dossier et entrez dedans :

```sh
mkdir docusaurus-ci-exam
cd docusaurus-ci-exam
npx create-docusaurus@latest my-website classic
cd my-website
npm run build
npm run serve
```

### 📌 Création du Git
initialisation repo
```sh
git init
git add .
git commit -m "chore: Initialisation du projet Docusaurus"
```