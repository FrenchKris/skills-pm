# Changelog

Toutes les évolutions notables de ce repo. Format inspiré de [Keep a Changelog](https://keepachangelog.com/fr/1.1.0/), numérotation [SemVer](https://semver.org/lang/fr/).

À chaque nouvelle version : mettre à jour le numéro dans `.claude-plugin/marketplace.json` **et** `plugins/pm-business/.claude-plugin/plugin.json`, ajouter une entrée ici, puis publier un tag `vX.Y.Z`.

## [Non publié]

### Ajouté
- `CLAUDE.md` : règles que Claude suit pour modifier ce repo (version, changelog, accord avant envoi).

### Prévu
- Skill `priorisation-arbitrage` (v0.2.0).
- Skill `gtm-launch` (v0.3.0).

## [0.1.0] - 2026-10-29

### Ajouté
- Structure marketplace Claude Code, plugin `pm-business`.
- Skill `discovery-business` : verbatims clients B2B → 5 hypothèses de valeur max, pondérées par le contexte stratégique.
- `contexte-entreprise.md` : les 4 questions de contexte stratégique et leur effet sur le classement.
- Exemple complet et fictif (entrée, sortie, biais détectés).
- README pour recruteurs, avec liens vers le portfolio et LinkedIn.
- Licence MIT.

[Non publié]: https://github.com/FrenchKris/skills-pm/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/FrenchKris/skills-pm/releases/tag/v0.1.0
