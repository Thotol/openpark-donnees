# OpenPark : données publiées

Ce dépôt ne contient que des données. La chaîne de données d'OpenPark, une application libre et sans compte qui dit où
se garer à Montréal, les produit et les publie ici ; l'application les télécharge de façon anonyme et fait tout le
calcul sur le téléphone. Le code de l'application et de la chaîne vit dans un autre dépôt.

## Ce qu'il contient

| Où | Contenu | Mise à jour |
|---|---|---|
| Release `donnees-montreal` | Manifeste, paquet SQLite compressé du Grand Montréal (côtés de rue, règles des panneaux, places tarifées, travaux, remorquages, bornes d'incendie, limites des villes et arrondissements, fond de carte régional) et deltas d'un jour à l'autre | Chaque jour, quand une source change |
| Branche `donnees-neige` | État du déneigement de chaque côté de rue de Montréal | Toutes les 10 minutes en saison. **Pas encore publiée** : la chaîne attend son jeton pour l'API Planif-Neige de la Ville |
| `fonds/` | Extraits d'OpenStreetMap qui donnent le fond de carte régional de Montréal et de Québec (eau, parcs, routes principales, noms de lieux) | Quelques fois par an, à la main |

Ces données décrivent les règles telles que les sources les publient. Les panneaux posés dans la rue font toujours foi.

## Sources et licences

Le paquet est une adaptation des jeux suivants. Chacun garde sa licence ; le paquet cite ses sources dans sa table
`meta`.

- **Ville de Montréal**, [portail de données ouvertes](https://donnees.montreal.ca), licence
  [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.fr) : Géobase, signalisation de stationnement sur rue,
  limites administratives, entraves et travaux, bornes d'incendie, îlots de voirie, stationnements gratuits pendant le
  déneigement, remorquages de véhicules gênants.
- **Agence de mobilité durable**, licence CC BY 4.0 : places et horaires de stationnement tarifé.
- **Ministère des Ressources naturelles et des Forêts du Québec**, sur [Données Québec](https://www.donneesquebec.ca),
  licence CC BY 4.0 : Référentiel québécois du réseau routier (RQRR) et découpages administratifs (SDA).
- **OpenStreetMap**, licence [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/) : la table `fond_carte` du
  paquet et les fichiers de `fonds/`. Cette table ne référence aucune autre table du paquet. Toute réutilisation doit
  porter la mention « © les contributeurs d'OpenStreetMap », et une base qui en dérive reste sous ODbL 1.0.

Pour réutiliser ces données, citez les sources ci-dessus, chacune selon sa licence.
