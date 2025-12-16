# Guide de Déploiement sur GitHub Pages

Ce guide vous explique comment déployer votre portfolio Hugo sur GitHub Pages.

## Prérequis

- Un compte GitHub
- Git installé sur votre ordinateur
- Le projet portfolio-claire prêt à être déployé

## Étapes de Déploiement

### 1. Créer un dépôt GitHub

1. Connectez-vous à [GitHub](https://github.com)
2. Cliquez sur le bouton "New repository" (Nouveau dépôt)
3. Nommez votre dépôt (exemple: `portfolio-claire` ou `username.github.io`)
4. Laissez le dépôt en **Public**
5. Ne cochez PAS "Initialize with README" (déjà présent)
6. Cliquez sur "Create repository"

### 2. Initialiser Git dans votre projet (si pas déjà fait)

```bash
cd portfolio-claire
git init
git add .
git commit -m "Initial commit: Portfolio Hugo"
```

### 3. Lier votre projet au dépôt GitHub

Remplacez `USERNAME` par votre nom d'utilisateur GitHub et `REPO` par le nom de votre dépôt:

```bash
git remote add origin https://github.com/USERNAME/REPO.git
git branch -M main
git push -u origin main
```

### 4. Activer GitHub Pages

1. Allez sur votre dépôt GitHub
2. Cliquez sur **Settings** (Paramètres)
3. Dans le menu de gauche, cliquez sur **Pages**
4. Sous "Build and deployment":
   - Source: Sélectionnez **GitHub Actions**
5. Le workflow `.github/workflows/deploy.yml` sera automatiquement détecté

### 5. Mise à jour du baseURL

Avant de déployer, mettez à jour le `baseURL` dans `hugo.toml`:

```toml
baseURL = 'https://USERNAME.github.io/REPO/'
```

Ou si vous utilisez un dépôt `username.github.io`:

```toml
baseURL = 'https://USERNAME.github.io/'
```

Puis commitez et poussez:

```bash
git add hugo.toml
git commit -m "Update baseURL for GitHub Pages"
git push
```

### 6. Vérifier le déploiement

1. Allez dans l'onglet **Actions** de votre dépôt GitHub
2. Vous verrez le workflow "Deploy Hugo site to GitHub Pages" en cours d'exécution
3. Attendez que le workflow soit terminé (environ 1-2 minutes)
4. Une fois terminé, votre site sera accessible à: `https://USERNAME.github.io/REPO/`

## Structure du Workflow

Le fichier `.github/workflows/deploy.yml` fait automatiquement:

1. **Installation de Hugo** (version 0.121.0)
2. **Checkout du code** avec les submodules (thème PaperMod)
3. **Build du site** avec `hugo --minify`
4. **Déploiement** sur GitHub Pages

## Mises à jour futures

Pour mettre à jour votre portfolio:

```bash
# Faites vos modifications
git add .
git commit -m "Description de vos modifications"
git push
```

Le site sera automatiquement reconstruit et redéployé!

## Domaine personnalisé (optionnel)

Si vous voulez utiliser votre propre nom de domaine:

1. Achetez un nom de domaine (ex: clairezobo.com)
2. Dans les paramètres GitHub Pages, ajoutez votre domaine personnalisé
3. Configurez les DNS de votre domaine:
   - Type A vers les IPs de GitHub:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - Ou CNAME vers `USERNAME.github.io`
4. Mettez à jour le `baseURL` dans `hugo.toml` avec votre domaine

## Problèmes courants

### Le site ne s'affiche pas correctement

- Vérifiez que le `baseURL` est correct dans `hugo.toml`
- Vérifiez que GitHub Pages est activé avec "GitHub Actions" comme source
- Attendez quelques minutes après le déploiement

### Le thème ne s'affiche pas

- Assurez-vous que le dossier `themes/PaperMod` existe
- Vérifiez que les submodules Git sont bien configurés:
  ```bash
  git submodule update --init --recursive
  ```

### Erreur lors du build

- Vérifiez les logs dans l'onglet "Actions" de GitHub
- Assurez-vous que tous les fichiers nécessaires sont commités
- Vérifiez qu'il n'y a pas d'erreurs de syntaxe dans `hugo.toml`

## Support

Pour toute question:
- Documentation Hugo: https://gohugo.io/documentation/
- Documentation GitHub Pages: https://docs.github.com/pages
- Thème PaperMod: https://github.com/adityatelange/hugo-PaperMod

---

**Votre portfolio est maintenant en ligne! 🎉**

URL: https://USERNAME.github.io/REPO/
