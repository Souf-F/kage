# KAGE — La Voie du Samouraï

> *"Connaître la voie, c'est marcher sur la voie."* — Miyamoto Musashi

Une expérience web immersive inspirée du **Go Rin No Sho** (五輪書) de Miyamoto Musashi. Temple japonais rendu en temps réel dans le navigateur via WebGL, sans framework, sans build step.

---

## Aperçu

```
┌─────────────────────────────────────────────────────┐
│                                                     │
│   KAGE  ·  LA VOIE DU SAMOURAÏ                     │
│                                                     │
│   ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  100%  │
│                                                     │
│   [ La Terre ]  [ L'Eau ]  [ Le Feu ]  [ Le Vide ] │
│                                                     │
│        Là où la discipline                          │
│        révèle l'essentiel.                          │
│                                                     │
│              ↓ Défiler pour entrer                  │
└─────────────────────────────────────────────────────┘
```

---

## Les 5 Roues

Chaque section correspond à un livre du **Go Rin No Sho** :

| # | Roue | Kanji | Thème |
|---|------|-------|-------|
| 01 | La Terre | 地 | Fondation — maîtriser les bases avant tout |
| 02 | L'Eau | 水 | Fluidité — s'adapter sans perdre son essence |
| 03 | Le Feu | 火 | Intensité — la présence totale au moment d'agir |
| 04 | Le Vent | 風 | Comparaison — connaître les autres styles |
| 05 | Le Vide | 空 | Au-delà de la technique — l'intention pure |

---

## Architecture technique

```
kage/
├── index.html                   ← Site complet (HTML + CSS + JS inline)
└── secret-pathways-assets/
    ├── three.min.js             ← Three.js r149 (moteur WebGL)
    └── fonts.css                ← Polices : Onest, NotoJP, Cormorant Garamond
```

### Pipeline de rendu

```
Navigateur
    │
    ├── CSS (styles, animations, parallaxe)
    │
    ├── Three.js r149
    │   ├── Scène 3D (temple, lune, arbres, lanternes)
    │   ├── Système de particules (feuilles, brume, reflets)
    │   └── Post-processing (bloom, grain, DOF)
    │
    └── JS vanilla
        ├── Scroll → progression des chapitres
        ├── Foreground stages (images parallaxe)
        └── Curseur custom + navigation
```

---

## Stack

- **HTML / CSS / JavaScript** — zéro framework, zéro build step
- **Three.js r149** — rendu WebGL 3D temps réel
- **GLSL** — shaders custom (eau, atmosphère, lune)
- **Agents IA** — site conçu et construit par une équipe d'agents Leonard Davinci

---

## Lancer en local

```bash
# Python (inclus sur macOS/Linux)
python3 -m http.server 8090

# Ouvrir dans le navigateur
open http://localhost:8090
```

> Nécessite un navigateur avec support WebGL2 (Chrome, Firefox, Edge, Safari 15+)

---

## Performances

| Métrique | Valeur |
|----------|--------|
| Rendu initial | ~3s (construction scène 3D) |
| FPS cible | 60 FPS |
| Poids total | ~900 KB |
| Dépendances externes | 1 (Three.js) |

---

## À propos

Miyamoto Musashi (1584–1645) — samouraï japonais, 60+ duels sans défaite, auteur du **Go Rin No Sho** écrit en 1645 dans une grotte, deux semaines avant sa mort. Philosophe, peintre, sculpteur.

> *"Ne faites rien d'inutile."*

---

**Portfolio :** [aeonlabs.fr](https://aeonlabs.fr/)
