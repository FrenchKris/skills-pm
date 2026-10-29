# Contexte stratégique de l'entreprise

Référencé par `SKILL.md` (étape 2). Il sert à pondérer les hypothèses : la même liste de verbatims ne donne pas le même classement selon la stratégie de l'entreprise.

## Les 4 questions

À poser **en un seul bloc**, jamais une par une. Ne poser que celles dont la réponse manque.

1. **Priorité de l'année** : acquisition, adoption, rétention ou expansion ?
2. **Position sur le marché** : leader, challenger ou niche ?
3. **Où perdez-vous** face aux concurrents ? (réponse libre : prix, intégrations, couverture fonctionnelle, sécurité, support…)
4. **Où gagnez-vous** face aux concurrents ? (réponse libre)

## Règles d'usage

- **Contexte déjà fourni** (dans la conversation, un document, un projet) : aucune question.
- **Contexte partiel** : poser uniquement les questions manquantes, toujours en un seul bloc.
- **« Je ne sais pas » ou pas de réponse** : continuer, et afficher en tête de la sortie « Contexte stratégique non renseigné, classement non pondéré ». Ne jamais bloquer.
- Les réponses 3 et 4 sont **libres** : les reprendre telles qu'écrites. Rapprocher une hypothèse d'un axe par le sens, pas par le mot.
- « Perd » et « gagne » sont **deux signaux distincts** : ne jamais les fusionner.

## Effet sur le classement

| Situation | Effet |
|---|---|
| Hypothèse sur un axe où l'entreprise **perd** | Défensive : monte en priorité, surtout si priorité = rétention ou acquisition |
| Hypothèse sur un axe où l'entreprise **gagne** | Taguée « avantage à protéger » : monte si position = challenger ou niche |
| Investissement sur un axe perdant sans lien avec la priorité de l'année | Taguée « rattrapage coûteux, à arbitrer » |
| Hypothèse qui revient à copier un concurrent hors positionnement | Signalée comme telle |

## Modèle à remplir (pour réutiliser le contexte)

```markdown
- Priorité de l'année :
- Position sur le marché :
- Où nous perdons :
- Où nous gagnons :
```
