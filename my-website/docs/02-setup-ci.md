# ⚙️ Configuration de l'Intégration Continue (CI) avec GitHub Actions 🚀

Ce document explique comment mettre en place un workflow **GitHub Actions** pour automatiser la construction et le déploiement de Docusaurus sur **GitHub Pages**.

---

## 1️⃣ 📂 Création du fichier de workflow GitHub Actions

Dans votre projet, créez le fichier suivant :

📌 **Chemin du fichier** :  

📌 **Contenu du fichier** :

```yaml
name: Deploy Docusaurus

on:
  push:
    branches:
      - main

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest

    steps:
      - name: 📥 Checkout repository
        uses: actions/checkout@v3

      - name: 🔧 Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: 18

      - name: 📦 Install dependencies
        run: |
          cd my-website
          npm install

      - name: 🏗️ Build Docusaurus
        run: |
          cd my-website
          npm run build

      - name: 🚀 Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          personal_token: ${{ secrets.GH_PAT }}
          publish_dir: ./my-website/build
          publish_branch: gh-pages

```

# 🔐 Configuration du Personal Access Token (GH_PAT)

## 📌 Pourquoi un Personal Access Token ?
GitHub Actions a besoin d’un **Personal Access Token (PAT)** pour **pousser** le build sur la branche `gh-pages`.  
Cela permet à GitHub Actions d’avoir les permissions nécessaires pour déployer le site.

## 📌 Générer un token GitHub

1. **Allez sur GitHub** → **Settings** → **Developer settings** → **Personal Access Tokens**  
2. Cliquez sur **Generate new token (classic)**  
3. **Cochez les permissions suivantes** :
   - ✅ `repo` (full control)
   - ✅ `workflow`
4. **Générez le token et copiez-le** immédiatement !  
   ⚠️ **Une fois la page fermée, il ne sera plus visible.**

---

## 📌 Ajouter le token en secret GitHub

1. **Allez sur** **Settings** → **Secrets and variables** → **Actions**
2. Cliquez sur **New repository secret**
3. **Remplissez les champs suivants :**
   - **Nom du secret** : `GH_PAT`
   - **Valeur** : **Collez votre token PAT**
4. **Cliquez sur "Save"** ✅

---

## 🎯 Résumé

- 🔐 **Le token `GH_PAT` est maintenant sécurisé dans les secrets du dépôt.**
- 🔄 **GitHub Actions pourra l'utiliser pour déployer votre site sur `gh-pages`.**
- 🚀 **Vous êtes prêt à automatiser votre déploiement !**


---