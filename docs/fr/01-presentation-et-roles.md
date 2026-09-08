---
title: "Presentation et roles"
description: "Parcours français x402 : presentation et roles."
---

# x402 : payer une ressource HTTP

x402 est un protocole de paiement pour accéder à une ressource : API, fichier ou service. Ce n’est pas un standard de token.
Le **client** choisit et autorise un paiement ; le **serveur** fournit la ressource ; le **facilitateur** vérifie et soumet le paiement selon le mécanisme retenu.
Le serveur peut aussi prendre en charge ces fonctions : un service tiers unique n’est pas imposé.
Les [spécifications](../../specs) décrivent le protocole ; les [SDK](../../typescript/packages) l’implémentent ; les [exemples](../../examples) montrent les intégrations.
**Piège :** supporter x402 ne signifie pas accepter tous les tokens et réseaux. Les participants doivent partager les combinaisons compatibles.

Source : [x402 Foundation](https://github.com/x402-foundation/x402), commit `4e15690028cf6d66b35e44a8128da47da9b92a4d` ; [licence Apache-2.0](../../LICENSE).

[Suite : Cycle HTTP et en tetes](02-cycle-http.md)
