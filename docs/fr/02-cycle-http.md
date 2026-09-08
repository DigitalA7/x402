---
title: "Cycle HTTP et en tetes"
description: "Parcours français x402 : cycle http et en tetes."
---

# Le cycle HTTP v2

Sans paiement, le serveur répond `402 Payment Required` avec les conditions dans `PAYMENT-REQUIRED`.
Le client choisit une offre et transmet son autorisation dans `PAYMENT-SIGNATURE`.
Le serveur vérifie puis organise le règlement ; dans le flux usuel, la ressource est renvoyée après succès avec `PAYMENT-RESPONSE`.
Ces en-têtes transportent du JSON encodé en Base64 : l’encodage n’est pas un chiffrement.
**Refus :** une autorisation absente ou invalide conduit à une demande de paiement, pas à un accès accordé. Les erreurs de règlement doivent également être traitées.
**Piège :** une vérification favorable ne prouve pas encore le règlement. Un timeout après diffusion demande une réconciliation, pas un nouveau paiement aveugle.

[Transport v2](../../specs/transports-v2/http.md) · [Serveur HTTP](../../typescript/packages/core/src/http/x402HTTPResourceServer.ts)

[Suite : Paiement exact sur EVM](03-paiements-evm.md)
