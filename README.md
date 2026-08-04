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
  logos/             wordmark, etc.
  frames/            hero-background (le grand visuel de l'email)
  speakers/          photos speakers (noms lisibles)
sgn-invest/          ← SGN Investment Summit (clair + monospace)
  logos/
  speakers/
shared/
  partner-logos/     logos partenaires communs aux deux
```

## Règles simples

- **Noms lisibles** (ex: `marc-lasry.jpg`), pas d'UUID.
- Un **dossier par summit** : on ne mélange jamais les chartes.
- Les logos partenaires communs vont dans `shared/`.

## À faire (suite)

- Migrer le reste des assets encore sur `sportgen-summit.vercel.app/email-assets/`
  (mur de logos partenaires, autres speakers) vers ce repo, avec des noms propres.
- Option : repointer les `reference.html` des playbooks vers ces URLs propres.
