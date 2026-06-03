# Livrables

Ce dossier contient tout ce que Claude produit pour toi : sites web, applications, scripts, outils.

---

## Règle d'or

| Quoi | Où |
|------|----|
| **Inputs** (documents que tu fournis : PDFs, exports, notes, briefs) | `context/import/` |
| **Outputs** (ce que Claude produit pour toi) | `livrables/` |

---

## Organisation

```
livrables/
├── sites-web/       # Sites internet, landing pages, portfolios
└── applications/    # Outils, scripts, automatisations, dashboards
```

---

## Convention de nommage

Format : `AAAA-MM-NOM-COURT`

Exemples :
- `2026-06-novaen-landing/`
- `2026-06-scraper-linkedin/`
- `2026-07-dashboard-ca/`

Règles :
- Tout en minuscules, tirets à la place des espaces
- Date au format `AAAA-MM` pour faciliter le tri chronologique
- Nom court mais descriptif (3-4 mots max)
- Un projet = un sous-dossier dédié
