---
title: "Paiement exact sur EVM"
description: "Parcours français x402 : paiement exact sur evm."
---

# Paiement exact sur EVM

Le schéma `exact` fixe le montant et le destinataire autorisés par le client ; le facilitateur paie le gas du règlement dans le parcours décrit.
Avec EIP-3009, le token accepte directement une autorisation de transfert signée, avec nonce et fenêtre de validité.
Avec Permit2, un contrat intermédiaire utilise une autorisation du token et une signature liée au transfert ; l’approbation initiale est une étape distincte.
La spécification décrit aussi une méthode ERC-7710 pour les comptes compatibles avec la délégation.
**Exemple :** `amount: "10000"` vaut 0,01 unité d’un actif à 6 décimales, pas 10 000 unités affichées.
**Piège :** un ERC-20 quelconque n’implémente pas nécessairement EIP-3009. Vérifier l’actif, le réseau et la méthode pris en charge.

[Spécification EVM](../../specs/schemes/exact/scheme_exact_evm.md) · [Livre Tokens](https://github.com/DigitalA7/openzeppelin-contracts/tree/master/docs/fr)

[Suite : Schemes et reseaux](04-schemas-de-paiement.md)
