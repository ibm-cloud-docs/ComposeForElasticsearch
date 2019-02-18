---
copyright:
  years: 2016,2018
lastupdated: "2018-06-18"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}

# Versions

Versions déployables| Version préférée
----------|-----------
2.4.6, 5.6.9, 6.2.2 | 6.2.2
{: caption="Tableau 1. Versions d'Elasticsearch" caption-side="top"}

## Version préférée

La version préférée est généralement la version la plus récente de la base de données Redis disponible pour {{site.data.keyword.composeForElasticsearch}}. Il s'agit de la version par défaut dans le sélecteur de version de la page du catalogue et également de la version automatiquement mise à disposition par l'API lorsqu'aucune version n'est spécifiée dans l'appel.

### Nouveau protocole de version préférée

Lorsqu'une nouvelle version est disponible, sa publication est annoncée et elle devient disponible pour déploiement. Après sa date de publication un délai d'environ 7 jours s'écoule pendant lequel la nouvelle version est disponible sans être la version préférée. Ce délai permet à nos utilisateurs de déployer et tester la nouvelle version tout en disposant toujours de la version en cours. Il permet également aux ingénieurs Compose de cibler et rectifier tout problème décelé dans la nouvelle version. Au bout de ce délai de 7 jours, la nouvelle version est définie en tant que version préférée ou une nouvelle date de modification est annoncée.

Vous trouverez la liste des versions disponibles pour mise à disposition sur la {{site.data.keyword.composeForMongoDB}} [page du catalogue](https://console.{DomainName}/catalog/services/compose-for-mongodb).

Pour obtenir la liste des versions actuellement disponibles pour votre service {{site.data.keyword.composeForElasticsearch}}, vous pouvez utiliser le
noeud final [GET /2016-07/deployments/:id/versions](https://apidocs.compose.com/v1.0/reference#2016-07-get-deployments-versions).
