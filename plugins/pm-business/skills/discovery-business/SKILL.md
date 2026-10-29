---
name: "discovery-business"
description: "Transforme des verbatims clients B2B (entretiens, tickets support, notes de Sales/CSM, avis) en 5 hypothèses de valeur maximum, rattachées à un rôle d'achat et à un levier SaaS, pondérées par le contexte stratégique de l'entreprise. À utiliser pour une discovery produit SaaS B2B. Hors cible : B2C."
---

# discovery-business

Conçu pour le SaaS B2B. Le skill ne génère pas de solutions : il produit des hypothèses de valeur à valider, classées.

## Entrées acceptées

Toute source de verbatims : entretiens, tickets support, notes de call commercial, notes de CSM, avis, réponses d'enquête. Le raisonnement ne change pas selon la source.

## Déroulé

### 1. Lecture des verbatims
- Relever la **provenance** de chaque verbatim : client direct, Sales, CSM, support.
- Rattacher chaque verbatim à un **rôle d'achat** : utilisateur, champion, décideur économique, payeur, bloqueur (IT, sécurité, achats). Rôle inconnu = verbatim signalé comme faible.
- Séparer ce qui est **dit** (citation exacte) de ce qui est **inféré** (interprétation).
- Classer à part les verbatims qui **citent un concurrent** : signal de positionnement, pas besoin produit.

### 2. Contexte stratégique
Appliquer `contexte-entreprise.md` (4 questions, posées en un seul bloc, jamais en cascade).
- Contexte déjà fourni : zéro question.
- Contexte partiel : poser uniquement les questions manquantes.
- « Je ne sais pas » : continuer, et afficher en tête « Contexte stratégique non renseigné, classement non pondéré ». Ne jamais bloquer.

### 3. Hypothèses
Pour chacune :
- **Un seul levier principal** : acquisition, adoption, rétention ou expansion.
- Format : *Qui (rôle d'achat) → problème observé → valeur business attendue → preuve dans les verbatims*.
- Signaler les biais : un seul compte, un seul profil, source indirecte (CSM ou Sales plutôt que client), gros compte réclamant du sur-mesure.

### 4. Pondération et tri
Les critères « perd » et « gagne » sont en réponse libre : les utiliser tels qu'écrits, sans les ramener de force à une liste fermée. Une hypothèse est rapprochée d'un critère par le sens, pas par le mot.
- Axe où l'entreprise **perd** → hypothèse défensive, monte en priorité (surtout si priorité = rétention ou acquisition).
- Axe où l'entreprise **gagne** → « avantage à protéger », monte si position = challenger ou niche.
- Investissement sur un axe perdant sans lien avec la priorité annuelle → « rattrapage coûteux, à arbitrer ».
- Hypothèse qui revient à copier un concurrent hors positionnement → le signaler.

## Sortie

Un seul tableau, **5 hypothèses maximum**, classées :

| # | Hypothèse | Rôle d'achat | Levier | Preuve (citations) | Alignement stratégique | Risque si faux | Test de validation |
|---|---|---|---|---|---|---|---|

- *Alignement stratégique* : fort / moyen / faible + une ligne (défensif, différenciant, ou rattrapage coûteux).
- *Test de validation* : concret et réaliste en B2B (appel avec 3 comptes comparables, analyse des deals perdus, lecture de tickets, prototype montré en rendez-vous de renouvellement). Jamais « faire des interviews » seul.
- Sous le tableau : verbatims concurrents (à part) et biais détectés, en quelques lignes.

## Ce que le skill refuse de faire

- Inventer un chiffre de valeur.
- Conclure « les clients veulent X » à partir de 2-3 citations, ou faire une hypothèse d'un verbatim isolé.
- Traiter une demande de Sales comme un besoin utilisateur validé.
- Produire des personas, des user stories ou reformuler les verbatims en solutions.
- Poser plus de 4 questions, ou en reposer si le contexte est donné.

## Cas de test (Doit / Ne doit pas)

- **Doit** produire un classement différent si la priorité passe d'acquisition à rétention.
- **Doit** produire un classement différent si l'axe « perd » est l'intégration plutôt que le prix.
- **Doit** taguer « avantage à protéger » une hypothèse alignée sur l'axe « gagne ».
- **Doit** classer à part un verbatim qui cite un concurrent.
- **Doit** signaler quand toutes les demandes viennent d'un seul compte ou d'un seul profil.
- **Ne doit pas** traiter « perd » et « gagne » comme un seul signal.
