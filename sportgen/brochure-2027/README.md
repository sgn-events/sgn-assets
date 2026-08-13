# SPORT[GEN] Summit 2027 — les assets de la brochure

Les images des 17 pages de la brochure 2027, telles que le deck les pose. Le
générateur qui les assemble vit dans
[sgn-deck-skill/brochure-2027](https://github.com/sgn-events/sgn-deck-skill/tree/master/brochure-2027).

Adresse publique : `https://sgn-assets.vercel.app/sportgen/brochure-2027/<fichier>`

## Ce qu'il y a dans chaque dossier

| Dossier | Quoi | Où c'est utilisé |
|---|---|---|
| `backgrounds/` | `slide-01.jpg` … `slide-17.jpg`, 1920x1080 | le fond plein cadre de chaque page. Une page = un fond, ils ne sont pas interchangeables |
| `portraits/` | 24 découpes de 255 px de large, coins arrondis cuits dans l'alpha | la grille des speakers (page 4) et celle du dîner VIP (page 7) |
| `quote-portraits/` | 6 vignettes de 138 px | les cartes de citations (page 5) |
| `photos/` | 7 photos recadrées exactement à leur boîte | pages 2, 6, 10 et les quatre visuels des pages packages |
| `charts/` | 2 donuts (page 3) et 2 cartes de graphiques (page 11) | posés tels quels, ce sont des images, pas des graphiques vivants |
| `press-icons/` | 4 icônes de 132 px | les cartes presse de la page 9 |
| `logos/` | les marques qui n'existent qu'en aplat sur le fond navy | voir ci-dessous |

## Les fichiers `-on-navy`

`mv-on-navy.png`, `ovni-capital-on-navy.png`, `bpifrance-on-navy.png`,
`unidentified-mark-on-navy.png` et `media-wall-on-navy.png` sont des **découpes
du rendu aplati** : le fond bleu nuit est dans l'image. Ce sont des pixels
d'origine, pas des reconstitutions, mais ils ne fonctionnent que posés sur ce
fond-là. Pour un email ou une page web, prendre les versions propres dans
`sportgen/logos/`.

`unidentified-mark-on-navy.png` est une marque du mur investisseurs que
personne n'a encore identifiée. Si vous savez de qui il s'agit, renommez le
fichier.

## Les marques propres sont ailleurs

Les logos utilisables partout (fond transparent, blanc) sont rangés un cran
au-dessus, parce qu'ils ne sont pas spécifiques à la brochure :

- `sportgen/logos/investors/` — Carlyle, Left Lane, Apex, Permira, 20VC,
  Headline, SLAM, Bromelia Capital, Crux Football
- `sportgen/logos/partners/` — AWS, Moët Hennessy, White & Case
- `sportgen/logos/media/` — les 20 marques médias (Sky, AFP, L'Équipe, Forbes,
  Le Point, Les Echos, France TV, BFM Business, M6, Canal+, TF1, RMC Sport,
  bein, Financial Times, La Gazzetta dello Sport, Maddyness, SportBusiness,
  Sport Business Club, Sport Buzz Business, Vibes)
- `sportgen/photos/` — les mêmes photographies, non recadrées
- `sportgen/speakers/` — les portraits bruts, avant découpe
