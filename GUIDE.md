# Guide d'Utilisation - Portfolio Claire

## 🚀 Démarrage rapide

### Lancer le site en local

```bash
cd portfolio-claire
hugo server -D --port 1314
```

Le site sera accessible sur : **http://localhost:1314**

### Arrêter le serveur

Appuyez sur `Ctrl+C` dans le terminal

## ✏️ Personnalisation

### 1. Informations personnelles

Modifiez le fichier [hugo.toml](hugo.toml):

```toml
title = 'Claire - Cybersecurity Portfolio'

[params.profileMode]
  title = "Claire"
  subtitle = "Cybersecurity Specialist | Epitech Student"
```

### 2. Liens sociaux

Dans [hugo.toml](hugo.toml), section `params.socialIcons`:

```toml
[[params.socialIcons]]
  name = "github"
  url = "https://github.com/votre-username"

[[params.socialIcons]]
  name = "linkedin"
  url = "https://linkedin.com/in/votre-profil"

[[params.socialIcons]]
  name = "email"
  url = "mailto:votre.email@example.com"
```

### 3. Photo de profil

1. Ajoutez votre photo dans `static/images/profile.jpg`
2. L'image est déjà configurée dans hugo.toml:
   ```toml
   imageUrl = "images/profile.jpg"
   ```

### 4. Modifier la page "À propos"

Éditez [content/about/index.md](content/about/index.md)

### 5. Ajouter/modifier vos compétences

Éditez [content/competences/index.md](content/competences/index.md)

### 6. Ajouter un nouveau projet

```bash
hugo new content/projets/nom-du-projet.md
```

Puis éditez le fichier créé avec votre contenu.

**Structure d'un projet :**

```markdown
---
title: "Titre du Projet"
date: 2025-12-16
draft: false
tags: ["Python", "Security", "Web"]
categories: ["Catégorie"]
description: "Description courte"
---

# Titre du Projet

Votre contenu ici...
```

### 7. Modifier vos informations de contact

Éditez [content/contact/index.md](content/contact/index.md)

## 🎨 Personnaliser les couleurs

### Modifier les couleurs roses

Éditez [assets/css/extended/custom.css](assets/css/extended/custom.css):

```css
:root {
    --primary-pink: #E91E63;      /* Rose principal */
    --secondary-pink: #FF4081;    /* Rose secondaire */
    --light-pink: #F8BBD0;        /* Rose clair */
    --dark-pink: #C2185B;         /* Rose foncé */
}
```

### Palette de couleurs suggérées

**Rose professionnel (actuel):**
- Primary: `#E91E63` - Material Design Pink 500
- Secondary: `#FF4081` - Material Design Pink A200

**Alternatives roses:**
- Rose poudré: `#FFB6C1`, `#FFC0CB`
- Rose vif: `#FF1493`, `#FF69B4`
- Rose saumon: `#FA8072`, `#FFA07A`

## 📝 Gestion du contenu

### Publier/Dépublier un contenu

Dans le front matter (en-tête) de chaque fichier markdown:

```markdown
---
draft: false  # Publié
---
```

ou

```markdown
---
draft: true   # Brouillon (non visible en production)
---
```

### Organiser vos projets

Les projets sont dans `content/projets/`. Vous pouvez:

1. **Créer des sous-dossiers** pour organiser par catégorie:
   ```
   content/projets/
   ├── web-security/
   │   └── scanner.md
   ├── forensics/
   │   └── honeypot.md
   └── ctf/
       └── writeups.md
   ```

2. **Utiliser les tags** pour filtrer:
   ```markdown
   tags: ["Python", "Web", "Security", "CTF"]
   ```

3. **Utiliser les catégories**:
   ```markdown
   categories: ["Sécurité Web", "Blue Team", "Red Team"]
   ```

## 🌐 Déploiement

### Option 1: GitHub Pages

1. Créez un repository GitHub
2. Poussez votre code:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/votre-username/portfolio.git
   git push -u origin main
   ```
3. Configurez GitHub Actions pour déployer automatiquement

### Option 2: Netlify

1. Connectez votre repository GitHub à Netlify
2. Configuration:
   - **Build command**: `hugo`
   - **Publish directory**: `public`
   - **Hugo version**: `0.152.2`

### Option 3: Vercel

1. Importez votre projet sur Vercel
2. La configuration Hugo est détectée automatiquement

## 🔧 Commandes utiles

```bash
# Créer un nouveau projet
hugo new content/projets/nom-du-projet.md

# Créer une nouvelle page
hugo new content/ma-page.md

# Serveur de développement (avec brouillons)
hugo server -D

# Serveur de développement (sans brouillons)
hugo server

# Générer le site statique pour production
hugo

# Générer et minifier
hugo --minify

# Nettoyer le cache
hugo mod clean
```

## 📊 Structure du site

```
portfolio-claire/
├── content/           # Contenu markdown
│   ├── about/        # Page À propos
│   ├── competences/  # Page Compétences
│   ├── projets/      # Articles de projets
│   └── contact/      # Page Contact
├── assets/           # Assets à traiter par Hugo
│   └── css/
│       └── extended/
│           └── custom.css  # CSS personnalisé
├── static/           # Fichiers statiques (copiés tels quels)
│   └── images/       # Images
├── themes/           # Thèmes Hugo
│   └── PaperMod/
├── hugo.toml         # Configuration principale
└── public/           # Site généré (git ignored)
```

## 🎯 Bonnes pratiques

### Images
- Placez les images dans `static/images/`
- Optimisez les images avant de les ajouter (compression)
- Utilisez des formats modernes (WebP, AVIF) si possible

### SEO
- Remplissez toujours le champ `description` dans le front matter
- Utilisez des titres descriptifs
- Ajoutez des tags pertinents

### Performance
- Évitez les images trop lourdes (max 500kb par image)
- Utilisez `hugo --minify` pour la production
- Activez la compression sur votre hébergeur

## 🆘 Dépannage

### Le site ne se lance pas
```bash
# Vérifier la version de Hugo
hugo version

# Lancer avec plus d'informations
hugo server -D --verbose
```

### Les styles ne s'appliquent pas
1. Vérifiez que `custom.css` est dans `assets/css/extended/`
2. Videz le cache du navigateur (Ctrl+F5)
3. Relancez le serveur Hugo

### Un projet n'apparaît pas
- Vérifiez que `draft: false` dans le front matter
- Assurez-vous que le fichier est dans `content/projets/`
- Relancez le serveur

## 📚 Ressources

- [Documentation Hugo](https://gohugo.io/documentation/)
- [Thème PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- [Markdown Guide](https://www.markdownguide.org/)
- [Material Design Colors](https://materialdesigncolors.com/)

---

**Besoin d'aide ?** Consultez le fichier [CLAUDE.md](../CLAUDE.md) pour l'historique complet du projet.
