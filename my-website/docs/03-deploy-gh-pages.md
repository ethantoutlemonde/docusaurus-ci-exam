# 🚀 Configuration de la branche `gh-pages` pour GitHub Pages

GitHub Pages nécessite une **branche dédiée** (`gh-pages`) pour héberger les fichiers du site.  
Cette section explique comment **créer et activer** cette branche.

---

## 📌 1️⃣ Création de la branche `gh-pages`

Exécutez les commandes suivantes pour **créer une branche vide `gh-pages`** :

```sh
git checkout --orphan gh-pages
git reset --hard  
git commit --allow-empty -m "Initial commit for GitHub Pages"
git push origin gh-pages  
git checkout main 
```
