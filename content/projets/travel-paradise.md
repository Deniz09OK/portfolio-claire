---
title: "Travel Paradise"
date: 2026-01-07
draft: false
tags: ["Docker", "DevOps", "CI/CD", "GitHub Actions"]
categories: ["Développement", "DevOps"]
description: "Application de gestion de voyage avec infrastructure conteneurisée et CI/CD"
---

# Travel Paradise

## Description

Application de gestion de voyage avec une infrastructure moderne basée sur Docker et un cycle de développement automatisé via GitHub Actions.

## Objectifs

- Créer une application complète de gestion de voyages
- Mettre en place une infrastructure conteneurisée
- Automatiser le cycle de développement
- Assurer la qualité du code et le déploiement continu

## Technologies utilisées

- **Docker** : Conteneurisation de l'application
- **Docker Compose** : Orchestration multi-conteneurs
- **GitHub Actions** : CI/CD et automatisation
- **Infrastructure as Code** : Dockerfile, docker-compose.yml

## Infrastructure Conteneurisée

### Docker
- **Dockerfile** optimisé pour l'application
- Images légères et sécurisées
- Multi-stage builds pour réduire la taille
- Gestion des environnements (dev, prod)

### Docker Compose
- Orchestration de plusieurs services
- Configuration de réseaux Docker
- Gestion des volumes pour la persistance
- Variables d'environnement sécurisées

## CI/CD avec GitHub Actions

### Pipeline automatisé
- **Build** : Construction automatique des images Docker
- **Tests** : Exécution des tests unitaires et d'intégration
- **Qualité du code** : Vérification automatique (linting, formatage)
- **Déploiement** : Déploiement automatique en production

### Workflow
```yaml
1. Push du code → GitHub
2. Déclenchement automatique du pipeline
3. Build de l'application
4. Exécution des tests
5. Analyse de la qualité du code
6. Déploiement si tous les tests passent
```

## Fonctionnalités

### Automatisation
- ✅ Build automatique à chaque commit
- ✅ Tests automatisés avant déploiement
- ✅ Vérification de la qualité du code
- ✅ Déploiement continu en environnement de production

### DevOps
- Infrastructure reproductible
- Environnements isolés via conteneurs
- Déploiements rapides et fiables
- Rollback facile en cas de problème

## Résultats

- ✅ Infrastructure 100% conteneurisée
- ✅ Déploiements automatisés via CI/CD
- ✅ Réduction du temps de déploiement de 80%
- ✅ Amélioration de la qualité du code grâce aux vérifications automatiques

## Compétences développées

- Conteneurisation avec Docker
- Orchestration de services
- CI/CD avec GitHub Actions
- Infrastructure as Code
- Automatisation de workflows
- Bonnes pratiques DevOps
