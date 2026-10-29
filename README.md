# Skills PM : le produit au service du business

Des skills Claude qui appliquent une méthode de Product Management **SaaS B2B** : partir de ce que disent les clients, et toujours relier une décision produit à un enjeu business (revenu, rétention, coût de vente).

Je suis **Kristel Lauverjon**, Product Manager certifiée (RNCP niveau 7, PSPO I), avec 10 ans en SaaS B2B : Sales grands comptes, puis Product Marketing. Ce repo montre ma façon de raisonner en produit. L'IA y sert d'outil, la méthode reste au centre.

## En 30 secondes

| Skill | Ce qu'il fait | Ce qu'il refuse de faire | Statut |
|---|---|---|---|
| [`discovery-business`](plugins/pm-business/skills/discovery-business/SKILL.md) | Transforme des verbatims clients en 5 hypothèses de valeur max, classées selon la stratégie de l'entreprise, avec un test de validation pour chacune | Inventer un chiffre, conclure sur 2 citations, prendre une demande Sales pour un besoin validé | ✅ Disponible |
| `priorisation-arbitrage` | Priorise un backlog puis force l'arbitrage business : revenu, coût de vente, capacité | | 🔜 À venir |
| `gtm-launch` | Plan de lancement : cible, message, canaux, KPI d'adoption à J+30/60/90 | | 🔜 À venir |

## Exemple : `discovery-business`

**Entrée** : 9 verbatims fictifs (entretiens, tickets, notes Sales et CSM) d'un éditeur RH, et son contexte : priorité *rétention*, position *challenger*, perd sur *les intégrations*, gagne sur *la simplicité*.

**Sortie** (extrait) :

| # | Hypothèse | Levier | Alignement stratégique | Test de validation |
|---|---|---|---|---|
| 1 | Double saisie entre SIRH et outil → menace le renouvellement | Rétention | **Fort**, défensif | Appeler 3 comptes qui renouvellent dans 6 mois ; relire les motifs de churn |
| 2 | Imports de fichiers peu fiables → friction de mise en route | Adoption | Moyen | Relire les tickets « import » des 6 derniers mois |
| 3 | Prise en main sans formation → soutient l'usage | Rétention | **Fort**, avantage à protéger | Mesurer le délai jusqu'au premier onboarding terminé |

Le skill écarte aussi, en le disant : un verbatim isolé, une demande sur-mesure d'un seul grand compte, et classe à part le verbatim qui cite un concurrent.

👉 [Voir l'exemple complet : entrée, sortie et biais détectés](exemples/discovery-business/README.md)

## Pourquoi ces choix

- **Peu de skills, mais testés.** Chaque skill définit ses entrées, sa sortie, ce qu'il refuse de faire et ses cas de test « Doit / Ne doit pas ».
- **Pas de générateur générique.** Pas de user stories, PRD vierges ou personas : ces outils existent déjà partout.
- **Le contexte change la réponse.** La même liste de verbatims donne un classement différent selon la priorité de l'année et la position marché.
- **Zéro donnée confidentielle.** Tous les exemples sont fictifs.

## Essayer

**Avec Claude Code** (2 commandes) :

```
/plugin marketplace add FrenchKris/skills-pm
/plugin install pm-business@skills-pm
```

**Avec claude.ai, sans Claude Code** : téléchargez le dossier [`discovery-business`](plugins/pm-business/skills/discovery-business), compressez-le en `.zip`, puis importez-le dans claude.ai depuis les paramètres, section Skills. Collez ensuite vos verbatims dans une conversation.

## Structure

```
skills-pm/
├── .claude-plugin/marketplace.json
├── plugins/pm-business/
│   ├── .claude-plugin/plugin.json
│   └── skills/discovery-business/
│       ├── SKILL.md                 # Le skill
│       └── contexte-entreprise.md   # Les 4 questions de contexte stratégique
└── exemples/discovery-business/     # Exemple complet entrée / sortie
```

## Licence

MIT. Réutilisez, adaptez, et dites-moi ce que vous en pensez.
