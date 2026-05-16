# Hachures Circulaires Croisées

**Générateur de tramage artistique pour traceur (plotter)**  
par [Martial Rossignol](http://www.martial-rossignol.fr) · Arras, France

---

## Aperçu

Hachures Circulaires Croisées est un outil web qui génère des compositions de **cercles concentriques superposés** dont la densité est modulée par la luminosité d'une image source. Il produit des fichiers SVG vectoriels prêts pour traceur plotter (AxiDraw, etc.) et des PNG haute résolution.

**[→ Essayer en ligne](https://rossignol-martial.github.io/Hachures-Circulaires-Croisees-v1.0/)**

---

## Fonctionnalités

- **N familles de cercles** (2 à 9 calques) avec centres indépendants
- Distribution automatique des centres sur un cercle paramétrable
- **Tramage tonal** : 5 zones de densité (seuils réglables)
- **Détection de contours** Sobel avec modes interpolé / additif
- **Prétraitement image** : gamma, CLAHE, flou gaussien
- Recadrage interactif avec poignées (ratio ⌃Ctrl, rotation ⇧Shift)
- Zoom / pan / fit sur le canvas
- Export **SVG** (calques séparés) et **PNG** aux formats papier (A5→A1, Letter)
- Système de **presets** nommés (localStorage)
- Interface 3 colonnes : paramètres | canvas | calques
- Fonctionne **100 % dans le navigateur**, sans serveur ni installation

---

## Utilisation

### Option 1 — En ligne
Ouvrir directement `index.html` dans un navigateur moderne (Chrome, Firefox, Safari).

### Option 2 — GitHub Pages
Forker ce dépôt et activer GitHub Pages sur la branche `main` depuis les Settings.

### Option 3 — Local
```bash
git clone https://github.com/rossignol-martial/hachures-circulaires-croisees
cd hachures-circulaires-croisees
# Ouvrir index.html dans le navigateur
open index.html
```

---

## Workflow rapide

1. **Glisser** une image JPG/PNG dans la zone de dépôt, puis passer en mode plein écran
2. **Recadrer** si nécessaire (bouton ⬚ dans la barre de zoom)
3. Choisir le **nombre de calques** (2–9) et leur répartition
4. Régler **pitch**, **seuils** et **contours**
5. Cliquer **⟳ générer**
6. **↓ exporter** → choisir format papier, marge, SVG ou PNG

---

## Paramètres clés

| Paramètre | Rôle |
|-----------|------|
| `pitch` | Espacement de base entre cercles (0.5–30 px) |
| `gamma` | Courbe tonale de l'image source |
| `CLAHE` | Égalisation locale du contraste |
| `contours` | Renforcement des bords (filtre Sobel) |
| `seuil bas/mi/haut/blanc` | 5 zones de densité discrètes |
| `rayon` | Distance des centres depuis le milieu de l'image |
| `rotation` | Angle de la constellation de centres |
| `jitter` | Perturbation organique des arcs |

---

## Export SVG pour traceur

Le SVG exporte chaque calque dans un groupe `<g id="calque1">` distinct.  
Dans **Inkscape** : activer chaque calque séparément pour les passes multicolores sur AxiDraw.

Le cadre est toujours inclus (trait noir 0.5 pt).

---

## Algorithme

Inspiré de la bibliothèque Python [plottertools/hatched](https://github.com/plottertools/hatched), transposé en JavaScript avec extensions :
- Multi-calques avec centres indépendants
- Détection de contours directionnelle (angle du gradient Sobel)
- CLAHE par grille 8×8 avec interpolation bilinéaire
- Perturbation déterministe (jitter) des rayons

---

## Licence

**CC BY-NC-SA 4.0** — Creative Commons Attribution Non-Commercial ShareAlike

© 2025 Martial Rossignol  
Vous pouvez partager et adapter ce travail à des fins non commerciales,  
à condition de citer l'auteur et de conserver la même licence.

[→ Texte complet de la licence](LICENSE)

---

## Auteur

**Martial Rossignol** — Photographe, Arras (Hauts-de-France)  
[martial-rossignol.fr](http://www.martial-rossignol.fr) · [@martialrossignol](https://instagram.com/martialrossignol)
