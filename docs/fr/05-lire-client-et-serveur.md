---
title: "Lecture du serveur et du client"
description: "Parcours français x402 : lecture du serveur et du client."
---

# Lire une intégration réelle

**Serveur :** l’[exemple Express](../../examples/typescript/servers/express/index.ts) protège `GET /weather` avec `paymentMiddleware`, configure `accepts`, puis enregistre les mécanismes acceptés. Il vérifie les variables de configuration avant de démarrer.
**Client :** l’[exemple Fetch](../../examples/typescript/clients/fetch/index.ts) configure le signataire, enregistre les schémas et utilise `wrapFetchWithPayment`. `processResponse` traite le résultat ; le `catch` final remonte les erreurs.
**Exercice de lecture :** retrouver le prix côté serveur, le réseau, le destinataire et le plafond `maxAmountPerPayment` côté client.
Repérer ensuite ce qui arrive quand aucune clé de signataire n’est configurée.
**Piège :** appeler ce client peut autoriser une dépense. Lire un exemple ne nécessite pas de le lancer ni de renseigner une clé réelle.

[Client HTTP](../../typescript/packages/core/src/http/x402HTTPClient.ts) · [Tests HTTP](../../typescript/packages/core/test/unit/http)

[Suite : Limites et verification documentaire](06-limites-et-verification.md)
