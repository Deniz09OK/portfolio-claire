---
title: "Scanner de Vulnérabilités Web"
date: 2025-12-15
draft: false
tags: ["Python", "Web Security", "OWASP", "Scanning"]
categories: ["Sécurité Web"]
description: "Outil automatisé de détection de vulnérabilités web"
---

# Scanner de Vulnérabilités Web

## Description

Développement d'un scanner automatisé de vulnérabilités pour applications web, capable de détecter les failles de sécurité courantes référencées dans l'OWASP Top 10.

## Objectifs

- Automatiser la détection de vulnérabilités web
- Identifier les failles OWASP Top 10
- Générer des rapports détaillés
- Proposer des recommandations de correction

## Technologies utilisées

- **Python 3** : Langage principal
- **Requests** : Pour les requêtes HTTP
- **BeautifulSoup** : Parsing HTML
- **Selenium** : Tests JavaScript
- **SQLMap** : Détection d'injections SQL

## Fonctionnalités

### Détection de vulnérabilités
- Injection SQL
- Cross-Site Scripting (XSS)
- CSRF
- Configuration de sécurité incorrecte
- Exposition de données sensibles
- Contrôle d'accès défaillant

### Reporting
- Génération de rapports HTML/PDF
- Classement par criticité (CVSS)
- Recommandations de correction
- Preuves de concept (PoC)

## Résultats

- ✅ Détection de 8 types de vulnérabilités différentes
- ✅ Taux de faux positifs < 5%
- ✅ Interface CLI conviviale
- ✅ Génération de rapports professionnels

## Apprentissages

Ce projet m'a permis de :
- Approfondir ma compréhension des vulnérabilités web
- Maîtriser les techniques d'automatisation en Python
- Comprendre les mécanismes de défense des applications web
- Développer des compétences en reporting de sécurité

## Code source

🔗 [GitHub Repository](https://github.com/)

---

*Projet réalisé dans le cadre de ma formation à Epitech*
