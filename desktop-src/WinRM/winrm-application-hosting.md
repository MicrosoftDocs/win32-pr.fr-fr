---
title: Infrastructure pour la gestion des services hébergés
description: Windows Remote Management 2,0 (WinRM) introduit une infrastructure d’hébergement. Pour utiliser le Framework, les plug-ins WinRM sont écrits et exposent les données de gestion d’une application au sein de l’infrastructure WinRM.
ms.assetid: 924dcc70-9a29-45a6-99a2-5681235e4574
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8439aca1f36d2d0c2cebb6ed3111aeaa2e4fcee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311308"
---
# <a name="infrastructure-for-managing-hosted-services"></a>Infrastructure pour la gestion des services hébergés

Windows Remote Management 2,0 (WinRM) introduit une infrastructure d’hébergement. Pour utiliser le Framework, les plug-ins WinRM sont écrits et exposent les données de gestion d’une application au sein de l’infrastructure WinRM. Deux modèles d’hébergement sont pris en charge. L’un est Internet Information Services (IIS) â € « based et l’autre est WinRMâ ». Le modèle WinRM utilise HTTP.sys et ne dépend pas d’IIS.

Les sections suivantes décrivent les modèles d’hébergement :

-   [Modèle d’hébergement d’extension IIS WinRM](#winrm-iis-extension-hosting-model)
    -   [Équilibrage de charge dans le modèle d’hébergement de l’extension WinRM IIS](#load-balancing-in-the-winrm-iis-extension-hosting-model)
    -   [Redirection HTTP dans le modèle d’hébergement de l’extension WinRM IIS](#http-redirection-in-the-winrm-iis-extension-hosting-model)
-   [Modèle d’hébergement du service WinRM](#winrm-service-hosting-model)

## <a name="winrm-iis-extension-hosting-model"></a>Modèle d’hébergement d’extension IIS WinRM

Le module d’extension IIS WinRM est un composant facultatif qui est installé à l’aide de l' **Gestionnaire de serveur**. Le module d’extension WinRM IIS est utilisé pour créer des points de terminaison WinRMâ» à partir du service IIS. Ce module peut être activé au niveau du site Web ou du répertoire virtuel. Il fonctionne en interceptant et en redirigeant les demandes entrantes vers le site Web ou le répertoire virtuel associé. Les requêtes sont redirigées vers un module WinRM qui analyse le contenu, puis détermine quel plug-in WinRM est configuré pour gérer chaque demande. Pour plus d’informations, consultez [configuration du plug-in hôte IIS](iis-host-plug-in-configuration.md).

Le modèle d’hébergement d’extension WinRM IIS est conçu pour gérer un grand nombre de requêtes. Si le modèle basé sur IIS est utilisé en tant qu’infrastructure d’hébergement, les fonctionnalités suivantes sont disponibles :

-   Les modules d’authentification IIS standard.
-   Processus du pool d’applications IIS pour héberger tous les plug-ins.
-   Gestion des quotas pour limiter les utilisateurs lourds du système. Pour plus d’informations, consultez [gestion de quota pour les shells distants](quotas.md).
-   Modèle de plug-in d’interpréteur de commandes. Voir [API du shell client WinRM](client-shell-api.md).
-   Modèle d’autorisation flexible. Voir [API du plug-in WinRM](winrm-plugin-api.md).

### <a name="load-balancing-in-the-winrm-iis-extension-hosting-model"></a>Équilibrage de charge dans le modèle d’hébergement de l’extension WinRM IIS

La plupart des équilibreurs de charge (lb) prennent en charge un modèle d’adhérence basé sur les cookies. Le LB insère un cookie dans la réponse à la première requête du client. Pour toutes les demandes suivantes, le cookie est transmis dans la demande et le LB utilise le cookie pour acheminer la demande vers le serveur approprié.

Dans les environnements où WinRM 2,0 est hébergé derrière un LB, le LB doit être configuré de façon à préfixer MS-WSMAN sur le nom du cookie. En outre, la LB doit être configurée pour permettre à la durée de vie du cookie d’être infinie, car le client WinRM doit contrôler la durée de validité du cookie.

Voici un exemple de nom de cookie :

``` syntax
MS-WSMAN=2046820362.20480.0000; path=/
```

### <a name="http-redirection-in-the-winrm-iis-extension-hosting-model"></a>Redirection HTTP dans le modèle d’hébergement de l’extension WinRM IIS

WinRM 2,0 peut gérer la redirection HTTP. Il est recommandé que toutes les redirections utilisent SSL (Secure Sockets Layer) (SSL) et que toutes les applications valident l’URI Redirigé avant de créer une nouvelle session.

## <a name="winrm-service-hosting-model"></a>Modèle d’hébergement du service WinRM

Le modèle de service WinRM s’exécute par-dessus HTTP.sys. Le service WinRM est un service réseau qui gère les demandes des clients WinRM. Le service détermine si la requête est routée vers un plug-in qui s’exécute dans le service principal ou est routé via un hôte où le plug-in tiers est exécuté. Ce modèle est destiné aux scénarios où la charge sur le nœud géré est faible. En outre, ce modèle est destiné aux scénarios dans lesquels l’hébergement IIS n’est pas une option. Pour plus d’informations, consultez [configuration du plug-in du service WinRM](wsman-service-plug-in-configuration.md).

 

 




