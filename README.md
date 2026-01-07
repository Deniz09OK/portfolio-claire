# Portfolio de Claire Estelle Zobo - Cybersécurité

Portfolio professionnel développé avec Hugo, présentant mon parcours en cybersécurité, réseaux et télécommunications.

## 👤 À propos

**Claire Estelle Zobo**
- Étudiante en Master 1 Cybersécurité à Epitech Nancy
- 5+ ans d'expérience en réseaux et télécommunications
- En recherche d'alternance en cybersécurité
- Localisation: Nancy, Grand Est, France

**Contact:**
- Email: claire-estelle.zobo@epitech.eu
- LinkedIn: [linkedin.com/in/claire-estelle-zobo](https://www.linkedin.com/in/claire-estelle-zobo)

## 🎨 Caractéristiques du Portfolio

- **Design**: Thème rose professionnel adapté à la cybersécurité
- **Framework**: Hugo v0.152.2 Extended (Static Site Generator)
- **Thème**: PaperMod (personnalisé)
- **SEO**: Optimisé avec meta descriptions, Open Graph, sitemap
- **Favicon**: Logo personnalisé rose avec initiales
- **Responsive**: Design adaptatif pour tous les appareils
- **Mode sombre**: Contraste amélioré pour une meilleure lisibilité

## 🚀 Démarrage Rapide

### Prérequis
- Hugo Extended (v0.112.0 ou supérieur)
- Git

### Installation et lancement local

```bash
cd portfolio-claire
hugo server -D --port 1314
```

Le site sera accessible sur `http://localhost:1314`

## 📁 Structure du Projet

```
portfolio-claire/
├── content/
│   ├── about/          # À propos - Parcours et objectifs
│   ├── competences/    # Compétences techniques (cybersécurité, réseaux, systèmes)
│   ├── experience/     # Expérience professionnelle (3 postes)
│   ├── projets/        # Portfolio de projets (3 exemples)
│   └── contact/        # Informations de contact et alternance
├── assets/
│   ├── css/extended/
│   │   └── custom.css  # Styles personnalisés (palette rose)
│   └── Profil.jpg      # Photo originale
├── static/
│   ├── images/
│   │   └── profile.jpg # Photo de profil (180x180px, ronde)
│   └── favicon.svg     # Favicon personnalisé (C rose)
├── themes/PaperMod/    # Thème Hugo (submodule Git)
├── .github/
│   └── workflows/
│       └── deploy.yml  # GitHub Actions pour déploiement automatique
├── hugo.toml           # Configuration principale
├── .gitignore          # Fichiers à ignorer
├── DEPLOYMENT.md       # Guide de déploiement détaillé
```

## 🎨 Palette de Couleurs

```css
--primary-pink: #E91E63     /* Material Design Pink 500 */
--secondary-pink: #FF4081    /* Material Design Pink A200 */
--light-pink: #F8BBD0        /* Rose pâle */
--dark-pink: #C2185B         /* Rose foncé */
--cyber-dark: #1a1a2e        /* Fond mode sombre */
--cyber-accent: #0f3460      /* Accent cybersécurité */
```

**Mode sombre:**
```css
--primary-pink: #FF6B9D      /* Rose plus clair pour meilleur contraste */
--secondary-pink: #FF4081
--light-pink: #4A2639        /* Rose très foncé */
```

## 💼 Sections du Portfolio

### 1. Page d'accueil
- Photo de profil ronde avec bordure rose
- Nom et titre professionnel
- Sous-titre: "Cybersécurité • Epitech Nancy • En recherche d'alternance"
- Boutons d'action: Projets, Compétences, Expérience, Contact
- Liens sociaux: LinkedIn, Email

### 2. À propos
- Présentation personnelle
- Parcours éducatif (BTS, Licence, ECOLE-IT, Epitech)
- Passion pour la cybersécurité
- Objectifs professionnels
- Qualités et compétences transversales

### 3. Compétences
- **Cybersécurité**: Analyse de vulnérabilités, audit réseau, pentesting
- **Réseaux**: Cisco, Mikrotik, VLANs, protocoles TCP/IP
- **Administration Systèmes**: Linux, Windows Server, virtualisation
- **DevOps**: Bash, PowerShell, Docker, CI/CD
- **Outils**: Nmap, Wireshark, Metasploit
- Formation et certifications

### 4. Expérience Professionnelle
- **Sh Tech** - Apprentie en Cybersécurité (9 mois, 2021-2022)
- **GLOPCOF** - Ingénieure Télécom Junior (1 an 9 mois, 2020-2021)
- **CRTVweb** - Technicienne Réseau et Télécom (4 mois, 2017)

### 5. Projets
Trois projets exemples à personnaliser:
- Scanner de vulnérabilités
- CTF Writeups
- Honeypot SSH

### 6. Contact
- Email et LinkedIn
- Localisation: Nancy, France
- Recherche d'alternance en cybersécurité
- Domaines d'intérêt: Red Team, Blue Team, DevSecOps
- Disponibilité et rythme souhaité

## 🔧 Commandes Utiles

```bash
# Lancer le serveur de développement
hugo server -D --port 1314

# Générer le site pour production
hugo --minify

# Créer un nouveau projet
hugo new content/projets/nom-projet.md

# Nettoyer les fichiers générés
rm -rf public resources
```

## 📦 Déploiement

### GitHub Pages (Recommandé)

Le projet inclut un workflow GitHub Actions (`.github/workflows/deploy.yml`) pour le déploiement automatique.

**Guide rapide:**
1. Créer un dépôt GitHub public
2. Modifier `baseURL` dans `hugo.toml`
3. Pousser le code sur GitHub
4. Activer GitHub Pages (Settings → Pages → Source: GitHub Actions)

**Documentation complète:** Voir `GITHUB-PAGES-QUICKSTART.md` et `DEPLOYMENT.md`

### Autres options de déploiement

- **Netlify**: Build command: `hugo`, Publish directory: `public`
- **Vercel**: Détection automatique Hugo
- **GitLab Pages**: Utiliser `.gitlab-ci.yml`

## ✨ Améliorations Apportées

### Design et UX
- ✅ Espacement vertical amélioré (2.5rem pour h2/h3/h4)
- ✅ Lisibilité accrue (line-height: 1.7)
- ✅ Transitions douces (0.3s ease) sur tous les liens
- ✅ Boutons avec effets hover prononcés
- ✅ Mode sombre avec meilleurs contrastes

### Composants Visuels
- ✅ Cartes de projets (.project-card) avec hover effects
- ✅ Timeline visuelle (.timeline) pour l'expérience professionnelle
- ✅ Icônes de sections (.section-icon) prêtes pour Font Awesome

### SEO et Performance
- ✅ Favicon personnalisé (favicon.svg)
- ✅ Meta descriptions optimisées
- ✅ Keywords: cybersécurité, pentesting, réseaux, etc.
- ✅ Open Graph tags pour réseaux sociaux
- ✅ Sitemap.xml généré automatiquement
- ✅ robots.txt activé
- ✅ Permaliens personnalisés

### Configuration
- ✅ Métadonnées masquées (hidemeta = true)
- ✅ Footer sans bordure
- ✅ Mention Hugo masquée
- ✅ Markup optimisé (unsafe HTML autorisé)

## 🎯 Prochaines Étapes Suggérées

### Court terme
1. Personnaliser les 3 projets exemples avec de vrais projets
2. Déployer sur GitHub Pages
3. Acheter un nom de domaine personnalisé (optionnel)
4. Créer un CV téléchargeable en PDF

### Moyen terme
5. Ajouter des certifications (CompTIA, CEH, etc.)
6. Créer un blog pour partager des articles de cybersécurité
7. Intégrer des badges de compétences (HackTheBox, TryHackMe)
8. Ajouter Google Analytics ou Plausible (optionnel)
9. Créer une page "Certifications"
10. Optimiser les images pour le web

## 📚 Documentation

- **CLAUDE.md**: Documentation complète de toutes les conversations et modifications
- **DEPLOYMENT.md**: Guide détaillé de déploiement
- **GITHUB-PAGES-QUICKSTART.md**: Guide rapide en 5 étapes
- **GUIDE.md**: Guide d'utilisation complet (si existant)
- **QUICKSTART.md**: Démarrage rapide (si existant)

## 🛠️ Technologies Utilisées

- **Hugo**: v0.152.2 Extended
- **Thème**: PaperMod (customisé)
- **CSS**: Custom CSS avec variables CSS
- **Deployment**: GitHub Actions
- **Hosting**: GitHub Pages (ou Netlify/Vercel)

## 📄 Fichiers Importants

- `hugo.toml`: Configuration principale du site
- `assets/css/extended/custom.css`: Styles personnalisés rose
- `content/`: Tous les contenus en Markdown
- `static/`: Images et fichiers statiques
- `.github/workflows/deploy.yml`: Workflow de déploiement
- `.gitignore`: Fichiers à ne pas commiter

## 🔐 Note sur la Sécurité

Ce portfolio met en avant des compétences en cybersécurité. Tous les exemples de projets de pentesting et d'exploitation de vulnérabilités mentionnés ont été réalisés dans des **environnements contrôlés** et **légaux**.

## 📞 Contact

Pour toute question concernant ce portfolio:
- **Email**: claire-estelle.zobo@epitech.eu
- **LinkedIn**: [Claire Estelle Zobo](https://www.linkedin.com/in/claire-estelle-zobo)

## 📝 Licence

Ce portfolio est un projet personnel. Le contenu est protégé par le droit d'auteur.

---

**Portfolio créé avec ❤️ et 🔐**

*Dernière mise à jour: Décembre 2025*
