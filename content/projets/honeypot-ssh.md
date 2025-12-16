---
title: "Honeypot SSH - Analyse d'Attaques"
date: 2025-12-05
draft: false
tags: ["Honeypot", "SSH", "Blue Team", "Forensics", "Python"]
categories: ["Sécurité Défensive"]
description: "Déploiement d'un honeypot SSH pour analyser les tentatives d'intrusion"
---

# Honeypot SSH - Analyse d'Attaques

## Description

Mise en place d'un honeypot SSH pour capturer et analyser les tentatives d'intrusion automatisées et les comportements des attaquants.

## Contexte

Les serveurs SSH sont constamment ciblés par des attaques automatisées (bruteforce, scan de ports). Ce projet vise à comprendre les techniques d'attaque et collecter des données sur les menaces.

## Architecture

### Infrastructure
- **Serveur** : VPS Debian 11
- **Honeypot** : Cowrie (honeypot SSH/Telnet)
- **Logging** : ELK Stack (Elasticsearch, Logstash, Kibana)
- **Alertes** : Telegram Bot pour notifications en temps réel

### Sécurité
- Isolation réseau complète
- Surveillance 24/7
- Aucune donnée sensible sur le honeypot
- Respect des lois sur la collecte de données

## Fonctionnalités

### Capture d'informations
- **Credentials** : Identifiants tentés lors des attaques
- **Commandes** : Commandes exécutées par les attaquants
- **Malwares** : Fichiers téléchargés pour analyse
- **Géolocalisation** : Provenance des attaques
- **Patterns** : Identification de comportements automatisés

### Analyse
- Dashboard Kibana pour visualisation
- Statistiques d'attaques en temps réel
- Classification des menaces
- Extraction d'IoC (Indicators of Compromise)

## Résultats (30 jours)

### Statistiques
- **43,000+** tentatives de connexion
- **2,500+** adresses IP uniques
- **150+** pays d'origine
- **500+** credentials uniques testés
- **15** malwares capturés et analysés

### Top des credentials tentés
1. `root:123456`
2. `admin:admin`
3. `root:password`
4. `ubuntu:ubuntu`
5. `pi:raspberry`

### Top des commandes exécutées
1. `wget` / `curl` (téléchargement de malware)
2. `uname -a` (reconnaissance système)
3. `/bin/busybox` (installation de botnet)
4. `cat /proc/cpuinfo` (information hardware)

### Pays sources principaux
1. 🇨🇳 Chine (35%)
2. 🇷🇺 Russie (22%)
3. 🇺🇸 États-Unis (15%)
4. 🇧🇷 Brésil (8%)
5. 🇮🇳 Inde (5%)

## Malwares analysés

### Mirai Botnet variant
- Botnet IoT classique
- Scan de ports automatisé
- Attaque DDoS
- Hash MD5 : `[hash]`

### Cryptocurrency miner
- Miner XMRig (Monero)
- Utilisation intensive CPU
- Persistance via crontab
- Hash MD5 : `[hash]`

## Enseignements

### Défense
- Importance de mots de passe forts
- Désactivation de l'authentification par mot de passe (utiliser des clés SSH)
- Changement du port SSH par défaut
- Fail2ban et rate limiting

### Attaque
- Les attaques SSH sont massivement automatisées
- Les botnets sont omniprésents
- Les attaquants privilégient les cibles faciles
- Pattern recognition pour identifier les scans

## Technologies utilisées

- **Python** : Scripts d'analyse et automatisation
- **Cowrie** : Honeypot SSH/Telnet
- **ELK Stack** : Analyse et visualisation de logs
- **Docker** : Containerisation
- **VirusTotal API** : Analyse de malware

## Améliorations futures

- [ ] Ajouter un honeypot HTTP/HTTPS
- [ ] Machine learning pour classification automatique
- [ ] Sandbox automatisée pour analyse de malware
- [ ] Partage de données avec la communauté (IoC)

## Ressources

🔗 [GitHub - Code source](https://github.com/)
🔗 [Dashboard public](https://dashboard.example.com/)
📊 [Rapport d'analyse complet (PDF)](https://example.com/report.pdf)

---

*Projet réalisé dans le cadre de mes études en Blue Team à Epitech*

⚠️ **Disclaimer** : Ce honeypot est déployé dans un cadre légal et éducatif, dans le respect de la législation sur la cybersécurité et la protection des données.
