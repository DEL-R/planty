# 🌿 Planty – Carnet botanique augmenté

> 🧭 Index général de navigation  
> 📍 Localisation : Balcon – Rouen (Nord-Est)  
> 📅 Dernière mise à jour : [[01_Journal/2025-06-14_Journal]]

---

## Alerte en cours : 

```dataview
TABLE date as "📅 Date", type as "⚡ Type", plantes as "🌿 Plantes concernées", notes as "📝 Observation"
FROM "05_Logs_Transversaux"
WHERE file.name = "Stress_Climatiques_2025"
  AND date >= date(today) - dur(1 day)
  AND date <= date(today) + dur(5 days)
  AND type != null
SORT date ASC
```
## 🌱 Plantes suivies

- [[03_Plantes/Aromates_Jumeaux]]
- [[03_Plantes/Coleus_Interieur]]
- [[03_Plantes/Radis_freres_du_Frigo]]
- [[03_Plantes/Menthes_Clan_d_Aveyron]]
- [[03_Plantes/Petunias_Clan_des_Trois]]
- [[03_Plantes/La_Mysterieuse_du_Pot_Terre]]
- [[03_Plantes/Mini_Rosiers_de_lIlot_Vert]]
- [[03_Plantes/Petunias_Clan_des_Trois]]

---

## 🪴 Zones du balcon

- [[02_PortesPlantes/Ilot_Vert]]
- [[Coin_Detente]]
- [[02_PortesPlantes/Face_Fenetre_Salon]]

---

## 📆 Journal des soins

- [[01_Journal/2025-06-12_Journal]]
- [[01_Journal/2025-06-13_Journal]]
- [[01_Journal/2025-06-14_Journal]]

---

## 🌤️ Suivi météo

- [[04_Meteo/Meteo_Semaine]]  
*(prévisions et impacts attendus)*

---

## 🧠 Logs transversaux

- [[05_Logs_Transversaux/Stress_Climatiques_2025]]  
*(événements climatiques notables et réactions)*

---

## 🧰 Templates disponibles

- [Fiche_Planty_Template](Fiche_Planty_Template.md)
- [Template_Meteo_Hebdo](Template_Meteo_Hebdo.md)

---

## 🔗 Navigation future (à ajouter)

- `[[Suivi_Visuel_Par_Semaine]]`
- `[[État_Général_Par_Espace]]`
- `[[Protocoles_Soins_Planty]]`