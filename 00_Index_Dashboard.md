#ĺ 🧭 Dashboard Planty — Suivi global du vivant  
> 🌱 Vue centralisée des soins, plantes, zones et événements  
> 🗓️ Dernière mise à jour : `2025‑06‑15`  
> 🔗 Inclus dans [[00_Index]]

---

## 🔧 Sommaire rapide  
- [[00_Index]]  
- [[01_Journal/]]  
- [[02_PortesPlantes/]]  
- [[03_Plantes/]]  
- [[04_Meteo/Meteo_Semaine]]  
- [[05_Logs_Transversaux/Stress_Climatiques_2025]]

---

## 🌿 Vue 1 — Derniers soins appliqués `#soin`

```dataview
TABLE date AS "📅 Date", zone AS "🏷️ Zone", tags AS "🏷️ Tags", file.link AS "🔗 Source"
FROM "01_Journal"
WHERE contains(tags, "#arrosage") OR contains(tags, "#taille") OR contains(tags, "#bouturage")
SORT date DESC
```


---

## ☀️ Vue 2 — Stress climatiques (météo / impact) #météo #stress_abiotique

```dataview 
TABLE date AS "📅 Date", type AS "⚡ Type", plantes AS "🌿 Impact", notes AS "📝 Notes"
FROM "05_Logs_Transversaux"
WHERE contains(file.name, "Stress_Climatiques")
SORT date DESC
```

---

## ☁️ Vue 2bis — Météo des 3 derniers jours (aperçu rapide)

```dataview
TABLE date AS "📅", type AS "☁️", notes AS "📝"
FROM "05_Logs_Transversaux"
WHERE file.name = "Stress_Climatiques_2025" AND date >= date(today) - dur(3 days)
SORT date DESC
```

---

## 🪴 Vue 3 — Plantes par zone #zones

```dataview
TABLE nom AS "🌿 Plante", zone AS "🪴 Zone", file.link AS "📂 Fiche"
FROM "03_Plantes"
WHERE zone
SORT zone ASC
```

---

## 🚨 Vue 4 — Plantes sensibles ou à risque #stress #à_surveillance

```dataview
TABLE nom AS "🌱 Nom", zone AS "🪴 Zone", tags AS "🏷️", file.link AS "📂 Fiche", notes AS "📝"
FROM "03_Plantes"
WHERE contains(tags, "#stress_") OR contains(tags, "#risque")
SORT nom ASC
```

---

## 🔄 Vue 5 — Déplacements / réaménagements #déplacement

```dataview 
TABLE date AS "📅 Date", file.link AS "📁 Entrée", text AS "📝 Mouvement"
FROM "01_Journal"
WHERE contains(text, "déplacé") OR contains(tags, "#déplacement")
SORT date DESC
```

---

## 🌸 Vue 6 — Suivi des floraisons #floraison

```dataview
TABLE date AS "📅 Date", zone AS "🪴 Zone", file.link AS "📁 Entrée"
FROM "01_Journal"
WHERE contains(text, "floraison") OR contains(tags, "#floraison")
SORT date DESC
```

---

## 📋 Vue 7 — Zones du balcon et contenu #porteplantes

```dataview 
TABLE file.link AS "📍 Zone", composition AS "🪴 Contenu"
FROM "02_PortesPlantes"
SORT file.name
```

---

## 📆 Vue 8 — Journal des 7 derniers jours #journal

```dataview
TABLE file.link AS "🗓️ Journal", date AS "📅"
FROM "01_Journal"
WHERE date >= date(today) - dur(7 days)
ÔSORT date DESC
```

---

## 🧭 Vue 9 — Fiches plantes orphelines (sans zone) #incomplet

```dataview 
TABLE nom AS "🌱 Nom", file.link AS "📁 Fiche"
FROM "03_Plantes"
WHERE !zone
```


---

## 🧪 Vue 10 — Plantes en expérimentation #expérimentation #bouture

```dataview 
TABLE nom AS "🧪 Plante", zone AS "🪴", tags AS "🔖", file.link
FROM "03_Plantes"
WHERE contains(tags, "#bouture") OR contains(tags, "#expérimentation")
```

---

## 🧼 Vue 11 — Plantes à surveiller (croissance lente ou repos) #à_surveiller #repos

```dataview 
TABLE nom AS "🌱 Nom", zone AS "🪴", tags AS "🔖", file.link
FROM "03_Plantes"
WHERE contains(tags, "#à_surveiller") OR contains(tags, "#repos") OR contains(tags, "#phase_lente")
```

---

## 📌 Notes

Toutes les vues reposent sur des conventions : tags::, zone::, nom::, composition::

Ce fichier est interopérable avec ton graphe sémantique Planty

Peut être intégré en [[00_Index]], dupliqué ou décliné par saison, ou archivé par année

Pour étendre ce tableau, pense à documenter les futurs soins saisonniers, maladies, floraisons majeures



---

## 🧠 Ce tableau de bord est ta boussole botanique : il montre les gestes, les fragilités et les évolutions de ton balcon en un seul coup d’œil, comme une carte vivante.