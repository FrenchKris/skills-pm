# Marketplace de skills : règles de modification

## Contexte

Ce dépôt est une marketplace **publique** de plugins et de skills Claude, qui sert de vitrine auprès de recruteurs. Les personnes qui te parlent ne sont pas des développeurs : explique tout en langage simple, sans jargon git.

**Règle d'or : tu ne fais jamais de commit sans avoir suivi le parcours ci-dessous, dans l'ordre. Si le numéro de version n'a pas changé, tu t'arrêtes et tu me le dis.**

**Repo public : aucune donnée personnelle ou confidentielle** (adresse e-mail, salaire, identifiants Notion, nom de client réel…). Les exemples restent fictifs. Les skills perso vont dans le repo privé `claude-skills`, jamais ici.

## Le parcours obligatoire

À chaque modification d'un skill, tu suis ces étapes, dans cet ordre :

1. **Synchroniser** : récupère la dernière version du dépôt (`git pull`) avant de toucher à quoi que ce soit.
2. **Modifier** : fais uniquement les changements demandés, dans le skill concerné.
3. **Incrémenter la version** du skill modifié (voir section suivante). Cette étape est obligatoire, même pour une simple virgule.
4. **Mettre à jour le changelog** : une entrée datée qui décrit le changement.
5. **Vérifier** : recopie la checklist ci-dessous dans ta réponse et coche chaque case.
6. **Résumer et demander accord** : explique en 3 à 5 lignes simples ce qui a changé, indique l'ancien et le nouveau numéro de version, puis attends mon « ok » explicite.
7. **Commit et envoi** : une fois l'accord reçu, fais le commit directement sur `main` avec un message clair, envoie-le sur GitHub (`git push`), puis publie l'étiquette de version `vX.Y.Z` (`git tag vX.Y.Z` puis `git push origin vX.Y.Z`).

## La règle de version

**Où se trouve le numéro :** la version est celle du plugin qui contient le skill (pas de version propre à chaque skill). Pour le plugin `pm-business`, elle est écrite à **deux endroits qui doivent toujours être identiques** :
- `plugins/pm-business/.claude-plugin/plugin.json` → champ `"version"`
- `.claude-plugin/marketplace.json` → champ `"version"` de l'entrée `pm-business`

**Changelog :** `CHANGELOG.md` à la racine, au format Keep a Changelog : une section `## [X.Y.Z] - AAAA-MM-JJ` avec des rubriques `### Ajouté`, `### Modifié`, `### Supprimé`, et les liens de comparaison en bas du fichier à jour.

**Quand l'incrémenter :** toujours, dès qu'un fichier du skill change. Aucune exception.

**De combien :**

| Type de changement | Exemple | Numéro |
|---|---|---|
| Correction de typo, reformulation | 1.2.3 → 1.2.**4** | patch |
| Nouvelle capacité, section ou fichier ajouté | 1.2.3 → 1.**3**.0 | minor |
| Changement qui casse l'usage existant | 1.2.3 → **2**.0.0 | major |

Si tu hésites entre deux niveaux, **pose-moi la question** avant de choisir.

Ne modifie jamais le numéro de version d'un skill que tu n'as pas touché.

## Checklist avant commit

Recopie et coche dans ta réponse :

- [ ] J'ai fait un `git pull` avant de commencer
- [ ] La version du skill modifié a été incrémentée (ancienne → nouvelle : ...)
- [ ] Le changelog contient une entrée pour ce changement
- [ ] Le skill a toujours son `SKILL.md` avec un frontmatter valide (name, description)
- [ ] Le README (tableau « En 30 secondes ») reflète le changement si besoin
- [ ] Aucune donnée personnelle ou confidentielle n'est incluse
- [ ] Aucun fichier parasite n'est inclus (brouillons, fichiers temporaires, `.DS_Store`)
- [ ] J'ai résumé les changements en langage simple et reçu un « ok »

## Façon de communiquer

- Dis « sauvegarder et envoyer mes changements » plutôt que « commit » et « push ».
- Si le résultat d'une commande git est incompréhensible pour un non-tech, traduis-le en une phrase.
- En cas de doute sur ce que je veux modifier, demande avant d'agir.

## Ce que tu ne fais jamais

- Pas de `git push --force`, jamais.
- Pas de suppression de fichiers, de skills ou d'historique sans me le demander explicitement.
- Pas de commit si la checklist n'est pas entièrement cochée.
- Pas de modification de skills autres que celui dont on parle.
- Si un `git pull` ou un `git push` échoue (conflit, refus), tu t'arrêtes, tu m'expliques simplement ce qui se passe, et tu attends mes instructions.

## Rappel final

**Version incrémentée ? Changelog à jour ? Rien de personnel ? Accord reçu ?** Si une réponse est non, tu ne commit pas.
