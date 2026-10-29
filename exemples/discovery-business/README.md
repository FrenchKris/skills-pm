# Exemple complet : `discovery-business`

> Cas **entièrement fictif**. « Talento » est un éditeur SaaS imaginaire de logiciel d'onboarding RH (ETI, 200 à 2 000 salariés). Aucune donnée réelle d'entreprise ou de client.

## Entrée

**Contexte stratégique**
- Priorité de l'année : rétention
- Position sur le marché : challenger
- Où nous perdons : les intégrations avec les SIRH
- Où nous gagnons : la simplicité de prise en main

**Verbatims**

| Réf | Source | Rôle | Verbatim |
|---|---|---|---|
| V1 | Entretien client, compte A | RH utilisatrice | « Je ressaisis chaque nouvel arrivant dans le SIRH puis dans Talento. Le lundi, j'y perds une heure. » |
| V2 | Note CSM, compte B | DRH | « Elle a demandé si on se connecte à Workday. Sinon, elle ne renouvelle pas en juin. » |
| V3 | Ticket support, compte C | Admin IT | « Import CSV en échec à cause des accents. Troisième ticket ce mois-ci. » |
| V4 | Note Sales, prospect D | Inconnu | « Ils nous comparent à Concurrent X, qui a une intégration Lucca native. » |
| V5 | Entretien client, compte A | Manager | « Mes nouveaux arrivants trouvent l'appli simple, pas besoin de formation. » |
| V6 | Entretien client, compte E | DAF | « Je ne vois aucun rapport qui montre ce que l'outil nous fait gagner. » |
| V7 | Note Sales, compte F (grand compte) | Inconnu | « Ils veulent un workflow différent par pays, sinon pas de signature. » |
| V8 | Avis en ligne | Inconnu | « Super outil, onboarding en 2 clics. » |
| V9 | Ticket support, compte H | RH utilisatrice | « Mon import de 40 salariés s'arrête à la ligne 12, sans message d'erreur. » |

## Sortie du skill

| # | Hypothèse | Rôle d'achat | Levier | Preuve (citations) | Alignement stratégique | Risque si faux | Test de validation |
|---|---|---|---|---|---|---|---|
| 1 | RH utilisatrices et DRH → double saisie entre SIRH et Talento → l'absence de synchronisation menace le renouvellement | Utilisateur + décideur économique | Rétention | V1 « je ressaisis… », V2 « sinon, elle ne renouvelle pas » | **Fort** : défensif (axe perdu = intégrations, priorité = rétention) | Construire des connecteurs coûteux qui ne changent pas la décision de renouvellement | Lister les comptes qui renouvellent dans les 6 mois, appeler 3 comptes sur le même SIRH, et relire les motifs de churn des 12 derniers mois |
| 2 | RH utilisatrices et admins IT → imports de fichiers peu fiables → friction dès la mise en route, coût support | Utilisateur + bloqueur (IT) | Adoption | V3 « troisième ticket ce mois-ci », V9 « s'arrête à la ligne 12 » | **Moyen** : lié à l'axe perdu (intégrations), correctif moins coûteux qu'un connecteur | Traiter un problème d'encodage ponctuel comme un sujet produit | Relire les tickets « import » des 6 derniers mois : volume, nombre de comptes touchés, délai de résolution |
| 3 | Managers et nouveaux arrivants → l'outil est pris en main sans formation → la simplicité soutient l'usage et le renouvellement | Utilisateur | Rétention | V5 « pas besoin de formation », V8 « 2 clics » | **Fort** : **avantage à protéger** (axe gagné, position challenger) | Sous-estimer l'effet d'ajouts complexes (ex. workflows par pays) sur cet avantage | Mesurer le délai jusqu'au premier onboarding terminé sur les 10 derniers comptes ; montrer un prototype enrichi à 3 managers en rendez-vous de suivi |

**Verbatim concurrent (à part)**
- V4 : Concurrent X met en avant une intégration Lucca native. Signal de positionnement, qui confirme l'axe perdu. Pas un besoin produit en soi.

**Biais et signaux écartés**
- V6 (DAF, mesure du ROI) : verbatim isolé, non transformé en hypothèse. À surveiller dans les prochains entretiens décideurs.
- V7 (workflow par pays) : demande Sales d'un seul grand compte, en sur-mesure. Non traitée comme un besoin validé ; entre en tension avec l'hypothèse 3.
- V2, V4, V7 viennent de sources indirectes (CSM, Sales).
- V8 : rôle inconnu, signal faible.
- V1 et V5 viennent du même compte A.

## Ce que l'exemple montre

- Avec la priorité **acquisition** au lieu de rétention, l'hypothèse 1 baisse et le positionnement face à Concurrent X prend plus de poids.
- Le skill refuse de faire une hypothèse d'un verbatim isolé (V6) et de traiter une demande Sales comme un besoin validé (V7).
- Aucun chiffre de valeur n'est inventé.
