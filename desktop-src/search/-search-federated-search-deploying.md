---
description: cette rubrique explique comment un utilisateur inscrit un nouveau magasin de données distant avec la recherche fédérée en ouvrant un fichier de Description de OpenSearch (. fichier osdx), en déployant un fichier. fichier osdx et en indiquant comment suivre l’utilisation de votre service OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: déployer des connecteurs de recherche dans Windows recherche fédérée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7515fa905abf3767696457f30a52abdb0a36d78883e9649cb2bf42e77e8b8c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463134"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a>déploiement de connecteurs de recherche dans Windows recherche fédérée

cette rubrique explique comment un utilisateur inscrit un nouveau magasin de données distant avec la recherche fédérée en ouvrant un fichier de Description de OpenSearch (. fichier osdx), en déployant un fichier. fichier osdx et en indiquant comment suivre l’utilisation de votre service [OpenSearch](https://github.com/dewitt/opensearch) .

Cette rubrique est organisée comme suit :

-   [Fichier. searchconnector-ms (connecteur de recherche)](#the-searchconnector-ms-search-connector-file)
-   [Méthodes de déploiement](#deployment-methods)
    -   [Déploiement par extraction](#pull-deployment)
    -   [Déploiement Push](#push-deployment)
-   [Suivi de l’utilisation](#tracking-usage)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>Fichier. searchconnector-ms (connecteur de recherche)

Il vous suffit d’ouvrir le fichier. fichier osdx qui décrit comment se connecter au service Web et de mapper les éléments personnalisés dans votre fichier. XML RSS ou Atom inscrit votre nouveau magasin de données distant avec la recherche fédérée. un magasin de données qui dispose déjà d’un service web [OpenSearch](https://github.com/dewitt/opensearch) qui est compatible avec la recherche fédérée peut être ajouté à Windows Explorer lorsqu’un utilisateur ouvre un fichier. fichier osdx.

Une fois que vous avez donné l’fichier osdx à votre utilisateur et que l’utilisateur ouvre le fichier. fichier osdx, les événements suivants se produisent.

1.  un fichier. searchconnector-ms est créé dans le dossier **recherches Windows** (% userprofile%/Searches).
2.  Un raccourci vers le fichier. searchconnector-MS est créé dans le dossier **des liens** (% UserProfile%/Links).
3.  un raccourci s’affiche dans le volet **favoris** de navigation Windows Explorer, ce qui permet à l’utilisateur de naviguer dans le nouveau magasin de données et d’interroger le service web.

## <a name="deployment-methods"></a>Méthodes de déploiement

Il existe deux façons de déployer des connecteurs de recherche, le déploiement par extraction et le déploiement push.

### <a name="pull-deployment"></a>Déploiement par extraction

Le déploiement par extraction décrit tout type de déploiement dans lequel l’utilisateur final prend l’initiative d’installer les connecteurs de recherche. Les méthodes courantes de déploiement par extraction sont les suivantes :

-   Attachement du fichier. fichier osdx dans un message électronique.
-   Publication du fichier sur une page Web.
-   Fournir un lien dynamique sur votre site intranet ; par exemple, un qui génère des fichiers. fichier osdx personnalisés en fonction des choix de l’utilisateur ou de l’étendue actuelle au sein du site.

Pour que le fichier soit téléchargé lorsque l’utilisateur clique sur le lien dans son navigateur, le serveur Web qui héberge le service Web doit être configuré pour remettre le fichier. fichier osdx en tant que fichier. Par conséquent, vous devez configurer les types MIME sur le serveur Web pour traiter les fichiers. fichier osdx comme `"application/opensearchdescription+xml"` . Si vous le souhaitez, vous pouvez utiliser l’icône fournie par Microsoft pour identifier le lien du connecteur de recherche.

### <a name="push-deployment"></a>Déploiement Push

Déploiement Push décrit tout type de déploiement qui ne dépend pas de l’initiative de l’utilisateur pour installer les connecteurs de recherche. Les méthodes courantes de déploiement Push sont les suivantes :

-   Préférences de stratégie de groupe (Préférences)
-   Script d’ouverture de session
-   Profils d’itinérance
-   Images

## <a name="tracking-usage"></a>Suivi de l’utilisation

pour suivre l’utilisation de votre service [OpenSearch](https://github.com/dewitt/opensearch) par les utilisateurs effectuant des recherches dans Windows Explorer, filtrez les fichiers journaux de votre serveur web pour cette chaîne d’agent utilisateur : `Windows-Search+(Windows+NT+6.1)` .

## <a name="additional-resources"></a>Ressources supplémentaires

pour plus d’informations sur l’implémentation de la fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Prise en main avec la recherche fédérée dans Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[connexion de votre Service web dans Windows recherche fédérée](-search-federated-search-web-service.md)
</dt> <dt>

[activation de votre magasin de données dans Windows recherche fédérée](-search-federated-search-data-store.md)
</dt> <dt>

[création d’un fichier de Description OpenSearch dans Windows recherche fédérée](-search-federated-search-osdx-file.md)
</dt> <dt>

[suivre les meilleures pratiques en matière de Windows la recherche fédérée](-search-fedsearch-best.md)
</dt> </dl>

 

 
