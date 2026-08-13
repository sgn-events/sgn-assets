# SGN Assets

Le dépôt central des images des emails (et autres visuels) des summits.
Rangé dans GitHub (versionné), **servi publiquement par Vercel** pour que les
images s'affichent dans les emails.

## Comment ça marche

- On **range** le fichier ici, dans GitHub → l'armoire (versionnée).
- Vercel est connecté à ce repo : **à chaque push, il republie automatiquement.**
- Chaque fichier devient accessible à une **adresse publique** (la vitrine) que
  les emails peuvent charger.

Personne ne fait d'upload manuel : on ajoute le fichier au bon dossier, on pousse,
c'est en ligne. (Ou on demande à l'agent de le faire.)

## Adresse publique (URL)

```
https://sgn-assets.vercel.app/<chemin-du-fichier>
```

Exemples :
- `https://sgn-assets.vercel.app/sportgen/logos/wordmark.png`
- `https://sgn-assets.vercel.app/sgn-invest/speakers/marc-lasry.jpg`

## Arborescence

```
sportgen/            ← summit SPORT[GEN] (sombre + doré)
  logos/             wordmark, lockup
    investors/       Carlyle, Permira, 20VC, Apex, Left Lane, Headline, SLAM…
    media/           Sky, AFP, L'Équipe, Forbes, Les Echos, Canal+, TF1…
    partners/        AWS, Moët Hennessy, White & Case
  frames/            hero-background (le grand visuel de l'email)
  photos/            photographies de l'événement, non recadrées
  speakers/          photos speakers (noms lisibles)
  ui/                éléments d'interface des emails
  brochure-2027/     les images de la brochure 17 pages — voir son README
sgn-invest/          ← SGN Investment Summit (clair + monospace)
  logos/
  speakers/
shared/
  partner-logos/     logos partenaires communs aux deux
  social/            icônes réseaux sociaux
templates/           gabarits d'emails HTML
```

Le dossier `sportgen/brochure-2027/` est particulier : ce sont les images du
deck de 17 pages, posées à des tailles précises. Son
[README](sportgen/brochure-2027/README.md) dit quoi sert où, et lesquelles
portent un fond navy cuit dans l'image (donc inutilisables ailleurs).

## Règles simples

- **Noms lisibles** (ex: `marc-lasry.jpg`), pas d'UUID.
- Un **dossier par summit** : on ne mélange jamais les chartes.
- Les logos partenaires communs vont dans `shared/`.

## À faire (suite)

- Migrer le reste des assets encore sur `sportgen-summit.vercel.app/email-assets/`
  (mur de logos partenaires, autres speakers) vers ce repo, avec des noms propres.
- Option : repointer les `reference.html` des playbooks vers ces URLs propres.
- Identifier la marque `sportgen/brochure-2027/logos/unidentified-mark-on-navy.png`
  (mur investisseurs) et la renommer.
- Un portrait du lot d'origine n'a pas été migré faute d'identification :
  `sgn-speaker-tbd.jpg` dans le dépôt du deck. Le nommer, puis l'ajouter à
  `sportgen/speakers/`.
