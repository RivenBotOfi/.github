# RivenBot

Bot Discord francophone — musique, modération, niveaux, salons vocaux temporaires
et tableau de bord web.

🌐 **[rivenbot.ca](https://rivenbot.ca)**

## Les dépôts

| Dépôt | Ce que c'est |
|---|---|
| [`RivenBot`](https://github.com/RivenBotOfi/RivenBot) | Le bot, l'API, le tableau de bord et le raccourcisseur d'URL — un seul dépôt, cinq services |

## Comment c'est déployé

Cinq processus PM2 à partir d'une base de code unique : le bot Discord, l'API du
tableau de bord, le raccourcisseur d'URL, le moniteur de statut et le serveur audio.
Chacun dans son propre conteneur, derrière un reverse proxy, sans aucun port ouvert
sur Internet — tout passe par un tunnel.
