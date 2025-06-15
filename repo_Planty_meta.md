---
id: repo_planty_meta
title: Dépôt GitHub Planty – Mémoire de référence
version: 1.0
type: meta_depot
tags:
  - structure
  - point_central
  - planty
  - git
  - mémoire_aug
  - obsidian
status: actif
date: 2025-06-14
source: https://github.com/DEL-R/planty
---

# 📦 `planty` — Dépôt GitHub de référence Planty

Ce dépôt GitHub constitue la **source de vérité du module `Planty`**, mémoire botanique augmentée basée sur Markdown + Obsidian.  
Il contient tous les fichiers nécessaires au suivi des plantes, des gestes de soin, des observations météorologiques, et des liens transversaux.

---

## 🔧 Fonctions principales

| Rôle              | Description                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------- |
| 🧭 Index central  | `00_Index.md` sert de table de navigation principale                                         |
| 🌿 Suivi vivant   | `01_Journal/`, `03_Plantes/`, `04_Meteo/` contiennent l’historique des soins et observations |
| 📊 Logs croisés   | `05_Logs_Transversaux/` regroupe les événements par type (ex. : stress climatique)           |
| 📁 Templates      | Tous les modèles sont dans `99_Templates/`                                                   |
| 🔗 Liens internes | Basés exclusivement sur `[[wikilinks]]` Obsidian                                             |

---

## 📁 Structure de référence (vue condensée)

- `00_Index.md` ← table d'entrée
- `01_Journal/` ← journal quotidien par date
- `02_PortesPlantes/` ← zones physiques du balcon
- `03_Plantes/` ← fiches plantes
- `04_Meteo/` ← météo hebdo ou historique
- `05_Logs_Transversaux/` ← stress, floraisons, événements transversaux
- `99_Templates/` ← modèles de fiche

---

## 🔐 Règle d’autorité

> Tout agent ou assistant s'appuyant sur `Planty` **doit considérer ce dépôt comme la version canonique**.  
> Toute modification locale ou en session doit être validée par synchronisation explicite avec ce dépôt.

---

## 🔄 Utilisations prévues

- 🌱 Base mémoire vivante d’un agent Planty ou d’un SMA personnel
- 📎 Synchronisation avec Obsidian local via Obsidian Git
- 🔁 Génération automatisée de rapports, synthèses, alertes

---

## 🔗 Dépendances et extensions prévues

- [[repo_Planty_Carte.md]] — carte du dépôt
- [[00_Index.md]] — point d'entrée logique
- `*.meta.md` — fichiers métas associés à chaque module