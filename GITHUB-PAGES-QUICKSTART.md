# Déploiement GitHub Pages - Guide Rapide

## 🚀 Déploiement en 5 minutes

### 1️⃣ Créer un dépôt GitHub

Allez sur GitHub et créez un nouveau dépôt **public** nommé `portfolio-claire`

### 2️⃣ Mettre à jour le baseURL

Ouvrez `hugo.toml` et modifiez la ligne:

```toml
baseURL = 'https://VOTRE-USERNAME.github.io/portfolio-claire/'
```

Remplacez `VOTRE-USERNAME` par votre nom d'utilisateur GitHub.

### 3️⃣ Initialiser Git et pousser

Dans le terminal, à la racine du projet:

```bash
cd portfolio-claire

git init
git add .
git commit -m "Initial commit: Portfolio Hugo"

git remote add origin https://github.com/VOTRE-USERNAME/portfolio-claire.git
git branch -M main
git push -u origin main
```

### 4️⃣ Activer GitHub Pages

1. Sur GitHub, allez dans votre dépôt
2. **Settings** → **Pages** (menu gauche)
3. Sous "Build and deployment", Source: **GitHub Actions**
4. C'est tout! ✨

### 5️⃣ Attendre et visiter

- Allez dans l'onglet **Actions**
- Attendez que le workflow soit terminé (1-2 minutes)
- Visitez: `https://VOTRE-USERNAME.github.io/portfolio-claire/`

---

## 📝 Pour les mises à jour futures

```bash
# Faites vos modifications...

git add .
git commit -m "Description des modifications"
git push
```

Le site sera automatiquement mis à jour!

---

## ⚠️ Note importante sur le thème

Le thème PaperMod doit être dans `themes/PaperMod/`. Si ce n'est pas le cas:

```bash
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
git submodule update --init --recursive
```

---

## 🎉 C'est fait!

Votre portfolio est maintenant en ligne et se met à jour automatiquement à chaque push!

**URL**: https://VOTRE-USERNAME.github.io/portfolio-claire/

---

## 📚 Besoin d'aide?

Consultez [DEPLOYMENT.md](DEPLOYMENT.md) pour le guide complet.
