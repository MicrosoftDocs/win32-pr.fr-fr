---
title: Récupération des informations
description: RTMv2 permet à un client de récupérer les informations référencées par un handle donné à l’aide des fonctions RtmGetEntityInfo, RtmGetDestInfo, RtmGetRouteInfo et RtmGetNextHopInfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058a87c9463011aec55b0c6c8c0574ff1e013f23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190851"
---
# <a name="retrieving-information"></a>Récupération des informations

RTMv2 permet à un client de récupérer les informations référencées par un handle donné à l’aide des fonctions [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)et [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .

Ces appels de fonction ont des fonctions correspondantes ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) pour libérer les handles associés à la structure d’informations retournée par le gestionnaire de tables de routage.

> [!Note]  
> Les informations pour les clients sont disponibles uniquement dans la famille d’adresses et d’instances actuelles.

 

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [Rechercher le meilleur itinéraire](search-for-the-best-route.md).

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a>Utilisation de RtmGetExactMatchRoute et RtmGetExactMatchDestination

Les fonctions [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) et [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) sont utilisées par les clients pour rechercher un itinéraire ou une destination spécifique. Ces fonctions permettent de gagner du temps en procédant au travail de comparaison pour le client.

Par exemple, lorsque RIP met à jour un itinéraire, RIP doit conserver les anciennes informations de métriques. RIP recherche l’itinéraire et ses informations. Ensuite, RIP peut copier les informations et mettre à jour l’itinéraire.

## <a name="using-rtmgetmostspecificdestination"></a>Utilisation de RtmGetMostSpecificDestination

La fonction [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) est utilisée pour localiser la destination qui correspond le mieux au préfixe réseau spécifié.

Par exemple, le gestionnaire de groupe de multidiffusion utilise cette fonction pour effectuer une vérification de transfert de chemin inverse (RPF) sur une seule adresse. La fonction peut également être utilisée pour rechercher le tronçon suivant local pour un tronçon suivant distant donné.

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [Rechercher des itinéraires à l’aide d’une arborescence de préfixe](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) et [recherchez le meilleur itinéraire](search-for-the-best-route.md).

## <a name="using-rtmgetlessspecificdestination"></a>Utilisation de RtmGetLessSpecificDestination

La fonction [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) est utilisée pour localiser la destination qui correspond à la meilleure correspondance pour le préfixe réseau spécifié. Cette fonction peut être appelée à plusieurs reprises pour retourner la correspondance suivante moins spécifique, jusqu’à ce qu’il n’y ait plus de destinations.

Cette fonction est appelée après un appel à [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).

Pour obtenir un exemple de code illustrant l’utilisation de ces fonctions, consultez [Rechercher des itinéraires à l’aide d’une arborescence de préfixe](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).

## <a name="using-rtmisbestroute"></a>Utilisation de RtmIsBestRoute

La fonction [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) permet à un client de déterminer rapidement si un itinéraire particulier est le meilleur itinéraire vers une destination. Par exemple, un client peut avoir besoin de stocker un itinéraire particulier uniquement s’il s’agit du meilleur itinéraire. Par conséquent, le client peut appeler cette fonction, au lieu d’énumérer tous les itinéraires et d’effectuer la comparaison elle-même.

 

 




