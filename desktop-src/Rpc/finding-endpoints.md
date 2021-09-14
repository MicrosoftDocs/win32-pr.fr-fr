---
title: Recherche de points de terminaison
description: Les programmes serveur écoutent les points de terminaison pour les demandes des clients. La syntaxe de la chaîne de point de terminaison dépend de la séquence de protocole que vous utilisez. Par exemple, le point de terminaison pour TCP/IP est un numéro de port, et la syntaxe du point de terminaison pour les canaux nommés est un nom de canal valide.
ms.assetid: 330bbe9f-b7e9-4a5b-86d8-824edec960d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0a97df3408a4d3c24dff9de28553f9e4b2210d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311533"
---
# <a name="finding-endpoints"></a>Recherche de points de terminaison

Les programmes serveur écoutent les points de terminaison pour les demandes des clients. La syntaxe de la chaîne de point de terminaison dépend de la séquence de protocole que vous utilisez. Par exemple, le point de terminaison pour TCP/IP est un numéro de port, et la syntaxe du point de terminaison pour les canaux nommés est un nom de canal valide.

Il existe deux types de points de terminaison : bien connus et dynamiques. Le choix du type de point de terminaison que votre programme utilise détermine si l’application distribuée ou la bibliothèque Runtime spécifie le point de terminaison.

Cette section traite des points de terminaison et présente des informations sur la façon de les trouver. Elle est organisée dans les rubriques suivantes :

-   [Utilisation de points de terminaison de Well-Known](#using-well-known-endpoints)
-   [Utilisation de points de terminaison dynamiques](#using-dynamic-endpoints)
-   [Exportation des points de terminaison Well-Known dans la base de données de mappage des points de terminaison](#exporting-well-known-endpoints-into-the-endpoint-map-database)

> [!Note]  
> Les termes *statiques des points de terminaison* et des *points de terminaison connus* sont équivalents et utilisés indifféremment.

 

Il est possible que votre application cliente utilise le mappage de point de terminaison pour déterminer si un programme serveur est en cours d’exécution. Votre client peut appeler [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)et [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) pour voir si le serveur a inscrit l’interface particulière dont il a besoin dans le mappage de point de terminaison.

## <a name="using-well-known-endpoints"></a>Utilisation de points de terminaison connus

Les points de terminaison connus sont des points de terminaison préattribués que le programme serveur utilise chaque fois qu’il s’exécute. Étant donné que le serveur écoute toujours ce point de terminaison particulier, le client tente toujours de s’y connecter. Les points de terminaison connus sont généralement affectés par l’autorité responsable du protocole de transport. Étant donné que les ordinateurs hôtes du serveur ont un nombre fini de points de terminaison disponibles, les développeurs d’applications sont fortement déconseillés d’utiliser des points de terminaison connus. Un autre avantage des points de terminaison dynamiques est qu’ils simplifient la gestion et la maintenance à long terme du système.

Une application distribuée peut spécifier un point de terminaison connu dans une chaîne et la passer en tant que paramètre à la fonction [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep). La chaîne de point de terminaison peut également apparaître dans l’en-tête d’interface de fichier IDL dans le cadre de l’attribut d’interface de \[ [point de terminaison](/windows/desktop/Midl/endpoint) \] .

Vous pouvez utiliser deux approches pour implémenter le point de terminaison connu :

-   Spécifier toutes les informations dans une liaison de chaîne
-   Stocker le point de terminaison connu dans la base de données de service de noms

Vous pouvez écrire toutes les informations nécessaires pour établir une liaison dans une application distribuée lorsque vous la développez. Le client peut spécifier le point de terminaison connu directement dans une chaîne, appeler [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) pour créer une chaîne qui contient toutes les informations de liaison et fournir cette chaîne à la fonction [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) pour obtenir un handle. Le client et le serveur peuvent être codés en dur pour utiliser un point de terminaison connu ou écrits afin que les informations de point de terminaison proviennent de la ligne de commande, d’un fichier de données, d’un fichier de configuration ou du fichier IDL.

Votre application cliente peut également interroger une base de données de service de noms pour obtenir des informations de point de terminaison bien connues.

## <a name="using-dynamic-endpoints"></a>Utilisation de points de terminaison dynamiques

Le nombre de points de terminaison pour un serveur particulier et une séquence de protocole particulière sont généralement limités. Par exemple, lorsque vous utilisez la séquence de protocole [ \_ \_ TCP IP ncacn](/windows/desktop/Midl/ncacn-ip-tcp) , qui indique que la communication réseau RPC se produit à l’aide de TCP/IP, seul un nombre limité de ports sont disponibles (la plupart des systèmes ont uniquement les plages 1025 à 5000 ouvertes). Les bibliothèques Runtime RPC vous permettent d’assigner des points de terminaison de manière dynamique, selon les besoins. Étant donné que le nombre d’UUID d’interface possibles est pratiquement illimité, l’utilisation de l’UUID d’interface pour diriger l’appel offre davantage d’espace pour l’extension et davantage de flexibilité.

Par défaut, les fonctions de la bibliothèque Runtime RPC recherchent les informations de point de terminaison lorsqu’elles interrogent une base de données de service de noms. Si le point de terminaison est dynamique, la base de données du service de noms ne contient pas d’informations de point de terminaison. Toutefois, la requête donnera au programme client le nom d’un serveur. Il peut ensuite rechercher le mappage du point de terminaison du serveur.

Si le client doit effectuer un appel de procédure distante à l’aide d’un point de terminaison dynamique, la méthode recommandée consiste à effectuer l’appel sur un handle de liaison partiellement lié. Le temps d’exécution RPC résout le point de terminaison en toute transparence. Cette méthode est supérieure à l’utilisation de la fonction [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding) , car elle permet des mécanismes de mise en cache avancés dans le temps d’exécution RPC.

Si un contrôle plus spécifique sur la sélection du point de terminaison est requis, les clients peuvent rechercher une entrée à la fois dans le mappage de point de terminaison en appelant les fonctions [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin), [**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)et [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) .

## <a name="exporting-well-known-endpoints-into-the-endpoint-map-database"></a>Exportation des points de terminaison connus dans la base de données de mappage des points de terminaison

Il est possible de mélanger les deux approches de recherche des points de terminaison, en particulier lorsqu’un système distribué passe d’un modèle de point de terminaison connu à un modèle de point de terminaison dynamique. Dans ces transitions, une version intermédiaire du serveur utilisera un point de terminaison connu, mais elle inscrira également le point de terminaison connu avec la base de données de mappage des points de terminaison. Cette approche permet aux clients qui utilisent un point de terminaison et des clients qui utilisent un point de terminaison dynamique de se connecter. Une fois que tous les serveurs ont été mis à niveau, vous pouvez déployer une nouvelle version du client qui utilise uniquement des points de terminaison dynamiques. Une fois que tous les clients ont été mis à niveau, une version de serveur finale peut cesser d’utiliser des points de terminaison connus et commencer à utiliser uniquement des points de terminaison dynamiques.

Cette approche permet un chemin de transition pour les applications qui ont démarré avec un point de terminaison connu, mais souhaitent migrer vers un point de terminaison dynamique sans nécessiter une mise à jour simultanée de tous les serveurs et clients.

 

 