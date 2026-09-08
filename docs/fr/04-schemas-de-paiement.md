---
title: "Schemes et reseaux"
description: "Parcours français x402 : schemes et reseaux."
---

# Schéma de paiement et réseau

`scheme` décrit comment la somme est due ; `network` indique où elle est réglée. Les deux doivent être compatibles côté client, serveur et facilitateur.
`exact` fixe une somme : par exemple un prix par appel d’API.
`upto` autorise un plafond ; le serveur règle l’usage réel dans cette limite.
`batch-settlement` sur EVM utilise séquestre et bons hors chaîne pour regrouper de petites dépenses avant règlement on-chain.
**Piège :** changer de réseau ne suffit pas à adapter un schéma. Signature, vérification et règlement dépendent de son implémentation.
Choisir explicitement le facilitateur et vérifier ses capacités ; un service public de démonstration ne constitue pas automatiquement un service de production.

[Schémas](../../specs/schemes) · [Choix d’intégration](../../README.md)

[Suite : Lecture du serveur et du client](05-lire-client-et-serveur.md)
