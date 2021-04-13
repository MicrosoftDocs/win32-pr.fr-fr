---
description: Cette rubrique explique comment un utilisateur inscrit un nouveau magasin de données distant avec la recherche fédérée en ouvrant un fichier de description OpenSearch (. fichier osdx), le déploiement d’un fichier. fichier osdx et le suivi de l’utilisation de votre service OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Déployer des connecteurs de recherche dans la recherche fédérée Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484440"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a>Déploiement de connecteurs de recherche dans la recherche fédérée Windows

Cette rubrique explique comment un utilisateur inscrit un nouveau magasin de données distant avec la recherche fédérée en ouvrant un fichier de description OpenSearch (. fichier osdx), le déploiement d’un fichier. fichier osdx et le suivi de l’utilisation de votre service [OpenSearch](https://github.com/dewitt/opensearch) .

Cette rubrique est organisée comme suit :

-   [Fichier. searchconnector-ms (connecteur de recherche)](#the-searchconnector-ms-search-connector-file)
-   [Méthodes de déploiement](#deployment-methods)
    -   [Déploiement par extraction](#pull-deployment)
    -   [Déploiement Push](#push-deployment)
-   [Suivi de l’utilisation](#tracking-usage)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>Fichier. searchconnector-ms (connecteur de recherche)

Il vous suffit d’ouvrir le fichier. fichier osdx qui décrit comment se connecter au service Web et de mapper les éléments personnalisés dans votre fichier. XML RSS ou Atom inscrit votre nouveau magasin de données distant avec la recherche fédérée. Un magasin de données qui dispose déjà d’un service Web [OpenSearch](https://github.com/dewitt/opensearch) compatible avec la recherche fédérée peut être ajouté à l’Explorateur Windows lorsqu’un utilisateur ouvre un fichier. fichier osdx.

Une fois que vous avez donné l’fichier osdx à votre utilisateur et que l’utilisateur ouvre le fichier. fichier osdx, les événements suivants se produisent.

1.  Un fichier. searchconnector-MS est créé dans le dossier **recherches Windows** (% UserProfile%/Searches).
2.  Un raccourci vers le fichier. searchconnector-MS est créé dans le dossier **des liens** (% UserProfile%/Links).
3.  Un raccourci s’affiche dans le volet **favoris** de navigation de l’Explorateur Windows, ce qui permet à l’utilisateur de naviguer dans le nouveau magasin de données et d’interroger le service Web.

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

Pour suivre l’utilisation de votre service [OpenSearch](https://github.com/dewitt/opensearch) par les utilisateurs effectuant des recherches à partir de l’Explorateur Windows, filtrez les fichiers journaux de votre serveur Web pour cette chaîne d’agent utilisateur : `Windows-Search+(Windows+NT+6.1)` .

## <a name="additional-resources"></a>Ressources supplémentaires

Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Prise en main avec la recherche fédérée dans Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connexion de votre service Web dans la recherche fédérée Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Activation de votre magasin de données dans la recherche fédérée Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Meilleures pratiques suivantes dans Windows Federated Search](-search-fedsearch-best.md)
</dt> </dl>

 

 
