---
description: Pourquoi Scale a choisi API Money, la solution de paiement pour marketplaces du groupe Orange, et à quoi elle servait.
---

# Paiement sécurisé avec API Money

## Qu'est-ce qu'API Money ?

**API Money** est une solution de paiement conçue pour les **marketplaces**. Elle est opérée par **W-HA, filiale à 100 % du groupe Orange**.

* W-HA est un **établissement de monnaie électronique agréé par l'ACPR** (le régulateur bancaire français) depuis 2013, avec un passeport européen.
* La solution est certifiée **PCI-DSS** (norme de sécurité des cartes bancaires).
* Elle respecte la **directive européenne sur les paiements (DSP2)** et les règles sur l'encaissement pour le compte de tiers.

## Pourquoi Scale en avait besoin

Scale est un intermédiaire : l'argent passe du **magasin** au **vendeur**. En Europe, encaisser de l'argent pour le compte d'autres personnes est une activité réglementée (directive DSP2). Il fallait donc un partenaire agréé pour le faire, et API Money était conçu exactement pour ce cas.

Trois raisons principales :

1. **La confiance.** Aucun des deux côtés ne prend de risque : l'argent du magasin est bloqué avant l'envoi, et le vendeur est sûr d'être payé si sa paire est authentique.
2. **La conformité.** API Money vérifie l'identité des utilisateurs et surveille les flux d'argent, comme l'exige la loi. Scale n'avait pas à devenir un établissement de paiement.
3. **La crédibilité.** S'appuyer sur une filiale du groupe Orange rassurait les magasins partenaires comme les vendeurs.

## À quoi API Money servait dans Scale

| Fonction | Dans Scale |
| --- | --- |
| **Portefeuilles électroniques** | Chaque magasin et chaque vendeur avait un portefeuille. Le magasin le rechargeait pour publier des demandes ; le vendeur y recevait ses paiements. |
| **Compte séquestre** | Au moment du deal, le montant de la paire était bloqué sur un compte sécurisé, puis libéré au vendeur après l'authentification. |
| **Vérification d'identité (KYC / KYB)** | Vérification des vendeurs particuliers (KYC) et des magasins (KYB) à l'inscription. |
| **Encaissement** | Recharge du portefeuille par carte bancaire ou virement. |
| **Virements sortants** | Transfert de l'argent du portefeuille vers le compte bancaire du vendeur. |

## Les frais

Les frais d'API Money (**1,2 %** par transaction) étaient inclus dans les frais vendeur de Scale. Le vendeur payait **4 % au total** au départ : 2,8 % pour Scale et 1,2 % pour le paiement. Les magasins ne payaient aucun frais.

Voir [Frais et niveaux vendeurs](frais-et-niveaux.md).

## Dans le développement

L'intégration de l'architecture API Money faisait partie du socle technique de la refonte de la plateforme, au même titre que la sécurité et la migration des données.

{% hint style="info" %}
Sources : site officiel [api-money.com](https://www.api-money.com/) et documents internes de Scale.
{% endhint %}
