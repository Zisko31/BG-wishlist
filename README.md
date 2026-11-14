# Ma liste de jeux de société

Site statique (GitHub Pages) pour consulter ma liste d'achats de jeux de société : filtres (joueurs, durée, règles, stratégie, hasard, mode, statut) et fiche détaillée par jeu (description, points forts et faibles, notes de plusieurs sites, récompenses, photos, liens).

## Fichiers

- `index.html` : la page (aucune dépendance, aucun build).
- `games.json` : toutes les données. C'est le seul fichier à modifier pour ajouter ou changer un jeu.
- `images/` : photos des jeux (facultatif).

## Ajouter ou modifier un jeu

Modifier `games.json` (directement sur GitHub avec le crayon, ou en demandant à Claude). Champs d'un jeu :

| Champ | Exemple | Rôle |
|---|---|---|
| `id` | `"arcs"` | identifiant unique, sans espace ni accent |
| `name`, `pitch`, `description` | texte | nom, résumé en une ligne, description (`\n` pour aller à la ligne) |
| `status` | `favori`, `etudier`, `achete`, `ecarte` | statut dans la liste |
| `playersMin`, `playersMax`, `playersBest` | `2`, `4`, `"3–4"` | nombre de joueurs |
| `durMin`, `durMax` | `60`, `120` | durée en minutes |
| `age`, `weight`, `price` | `14`, `3.4`, `75` | âge mini, complexité BGG /5, prix approx. en € |
| `rules`, `strategy`, `luck`, `twoPlayer` | `1` à `5` | règles (1 simple → 5 dur), stratégie, hasard, qualité à 2 |
| `modes` | `["compet"]` | `compet`, `coop`, `equipe` |
| `image`, `photos` | `"images/arcs.jpg"` ou une URL | photo principale et galerie |
| `pros`, `cons`, `awards` | listes de textes | points forts, faibles, récompenses |
| `ratings` | `{"site": "BoardGameGeek", "score": 8, "max": 10, "count": 1000, "url": "…", "note": "…"}` | notes des sites (`score: null` si pas de note chiffrée) |
| `links` | `{"label": "…", "url": "…"}` | liens utiles |
| `myNote` | texte | notes perso |

Penser aussi à mettre à jour `updatedAt` en haut du fichier.
