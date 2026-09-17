# RivenBot

Bot Discord francophone — musique, modération, niveaux, salons vocaux temporaires
et tableau de bord web.

🌐 **[rivenbot.ca](https://rivenbot.ca)**

## Les dépôts

| Dépôt | Ce que c'est |
|---|---|
| [`RivenBot`](https://github.com/RivenBotOfi/RivenBot) | Le bot Discord, l'API, le raccourcisseur d'URL et le moniteur de statut |
| [`rivenbot-dashboard`](https://github.com/RivenBotOfi/rivenbot-dashboard) | Le tableau de bord web — React, TypeScript, Vite, Tailwind |

## Pourquoi deux dépôts et pas cinq

Le tableau de bord est séparé parce qu'il l'est réellement : 169 fichiers
TypeScript qui n'importent **aucun** fichier du serveur, avec leur propre build.

Les quatre services backend restent ensemble, et c'est délibéré — ils partagent
31 modèles de données importés par 178 fichiers. Les séparer imposerait
d'extraire un paquet commun et de réécrire ces 178 imports, sans rien gagner.

## Déploiement

Cinq processus PM2, chacun dans son conteneur, derrière un reverse proxy.
Aucun port ouvert sur Internet : tout passe par un tunnel.
