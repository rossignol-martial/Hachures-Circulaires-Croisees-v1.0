# Roadmap — Hachures Circulaires Croisées

*Martial Rossignol · CC BY-NC-SA 4.0*

---

## En cours 

### Filtre de contour pour améliorer la lisibilité de l'image

## Prochaines versions

### Manuel utilisateur — révision complète

Le manuel actuel (`Manuel_Hachures_Circulaires_MR_v1.docx`) doit être mis à jour pour refléter l'évolution récente de l'interface :

- **Nouvelles fonctionnalités à documenter**
  - Calques Canny multiples (colonne droite, accordéons indépendants, œil global)
  - Bouton ↑ image dans le header + barre de transformation (rotation, flip)
  - Export SVG : calques Inkscape natifs (`inkscape:groupmode="layer"`)
  - Export PNG : option image source sous la trame
  - Panel Presets flottant et déplaçable
  - Drag & drop de l'image sur le canvas
  - Nommage automatique des exports à la date du jour
- **Captures d'écran à refaire** — l'interface a évolué significativement depuis la dernière version
- **Galerie d'exemples** — enrichir avec de nouveaux rendus illustrant les calques Canny
- **Révision de la section traceur** — ajout de recommandations pour les épaisseurs de trait selon le format papier (A0 à A5)

### Version anglaise

Produire une version anglaise complète du manuel :

- `Manuel_Hachures_Circulaires_MR_v1_EN.docx`
- Traduction de l'interface (labels, tooltips, messages) en option via un fichier de langue JSON
- README.md : section anglaise intégrée ou fichier `README_EN.md` séparé
- Description GitHub et topics déjà en anglais ✓

---

## Idées en réflexion

| Idée | Complexité | Intérêt |
|------|-----------|---------|
| Undo / Redo (Ctrl+Z) | haute | ★★★★ |
| Presets de démonstration embarqués | faible | ★★★★ |

---

## Versions publiées

| Version | Date | Notes |
|---------|------|-------|
| v1.0 | 2026 | Première publication — hachures circulaires, 2–9 calques, export SVG/PNG |
| v1.1 | 2026-05 | Calques Canny multiples, FDoG (abandonné), interface redessinée, presets flottants |

---

*Les contributions et retours sont les bienvenus via les [Issues GitHub](https://github.com/rossignol-martial/hachures-circulaires-croisees/issues).*
