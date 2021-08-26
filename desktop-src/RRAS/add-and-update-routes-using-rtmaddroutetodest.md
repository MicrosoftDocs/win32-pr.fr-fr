---
title: Ajouter et mettre à jour des itinéraires à l’aide de RtmAddRouteToDest
description: La fonction RtmAddRouteToDest est utilisée pour ajouter de nouveaux itinéraires et mettre à jour des itinéraires existants pour une destination. Les procédures suivantes expliquent les deux cas. L’exemple de code suivant montre comment implémenter la première procédure.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64032aa5f73019e08bb82405d85ffa5ef85abd0526cf7748ec8881b97ab900e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030599"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a>Ajouter et mettre à jour des itinéraires à l’aide de RtmAddRouteToDest

La fonction [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) est utilisée pour ajouter de nouveaux itinéraires et mettre à jour des itinéraires existants pour une destination. Les procédures suivantes expliquent les deux cas. L’exemple de code suivant montre comment implémenter la première procédure.

**Pour ajouter un itinéraire, le client doit effectuer les étapes suivantes**

1.  Si le client a déjà mis en cache le descripteur de saut suivant, passez à l’étape 4.
2.  Créez une structure d' [**\_ \_ informations de tronçon RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) et remplissez-la avec les informations appropriées.
3.  Ajoutez le tronçon suivant à la table de routage en appelant [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). Le gestionnaire de tables de routage retourne un handle vers le tronçon suivant. Si le tronçon suivant existe déjà, la table de routage n’ajoute pas le tronçon suivant. au lieu de cela, elle retourne le handle vers le tronçon suivant.
4.  Créez une structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) et remplissez-la avec les informations appropriées, y compris le descripteur de saut suivant renvoyé par le gestionnaire de tables de routage.
5.  Ajoutez l’itinéraire à la table de routage en appelant [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest). Le gestionnaire de tables de routage compare le nouvel itinéraire aux itinéraires qui se trouvent déjà dans la table de routage. Deux itinéraires sont égaux si toutes les conditions suivantes sont remplies :

    -   L’itinéraire est ajouté à la même destination.
    -   L’itinéraire est ajouté par le même client que celui spécifié par le membre **propriétaire** de la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .
    -   L’itinéraire est publié par le même voisin que celui spécifié par le membre **voisin** de la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .

    Si l’itinéraire existe, le gestionnaire de tables de routage retourne le descripteur à l’itinéraire existant. Dans le cas contraire, le gestionnaire de tables de routage ajoute l’itinéraire et retourne le descripteur au nouvel itinéraire.

    Le client peut définir le *paramètre \_ indicateurs de modification* sur la version RTM \_ \_ changer \_ nouveau pour indiquer au gestionnaire de tables de routage d’ajouter un nouvel itinéraire sur la destination, même s’il existe un autre itinéraire avec les mêmes champs propriétaire et voisin.

    Le client peut définir le *paramètre \_ indicateurs de modification* sur RTM \_ route \_ change \_ en premier pour indiquer au gestionnaire de tables de routage de mettre à jour le premier itinéraire sur la destination appartenant au client. Cette mise à jour peut être effectuée si un tel itinéraire existe, même si le champ voisin ne correspond pas. Cet indicateur est utilisé par les clients qui gèrent un seul itinéraire par destination.

**Pour mettre à jour un itinéraire, le client doit effectuer les étapes suivantes**

1.  Appelez [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) avec le descripteur de l’itinéraire. Le handle est soit un précédemment mis en cache par le client, soit retourné par le gestionnaire de table de routage à partir d’un appel qui retourne un handle d’itinéraire tel que **RtmGetRouteInfo**.
2.  Apportez les modifications à la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) qui est retournée par le gestionnaire de tables de routage.
3.  Appelez [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) avec le handle vers l’itinéraire et la structure [**d' \_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) modifiée.

L’exemple de code suivant montre comment ajouter un itinéraire à une destination à l’aide du gestionnaire de table de routage comme intermédiaire.


```C++
// Add a route to a destination given by (addr, masklen)
// using a next hop reachable with an interface

RTM_NEXTHOP_INFO NextHopInfo;

// First, create and add a next hop to the caller's
// next-hop tree (if it does not already exist)

ZeroMemory(&NextHopInfo, sizeof(RTM_NEXTHOP_INFO);

RTM_IPV4_MAKE_NET_ADDRESS(&NextHopInfo.NextHopAddress,
                          nexthop, // Address of the next hop
                          32);

NextHopInfo.InterfaceIndex = interface;

NextHopHandle = NULL;

Status = RtmAddNextHop(RtmRegHandle,
                       &NextHopInfo,
                       &NextHopHandle,
                       &ChangeFlags);

if (Status == NO_ERROR)
{
    // Created a new next hop or found an old one

        // Fill in the route information for the route
    
    ZeroMemory(&RouteInfo, sizeof(RTM_ROUTE_INFO);

    // Fill in the destination network's address and mask values
    RTM_IPV4_MAKE_NET_ADDRESS(&NetAddress, addr, masklen);

    // Assume 'neighbour learnt from' is the first next hop
    RouteInfo.Neighbour = NextHopHandle;

    // Set metric for route; Preference set internally
    RouteInfo.PrefInfo.Metric = metric;

    // Adding a route to both the unicast and multicast views
    RouteInfo.BelongsToViews = RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST;

    RouteInfo.NextHopsList.NumNextHops = 1;
    RouteInfo.NextHopsList.NextHops[0] = NextHopHandle;

    // If you want to add a new route, regardless of
    // whether a similar route already exists, use the following 
    //     ChangeFlags = RTM_ROUTE_CHANGE_NEW;

    ChangeFlags = 0;

    Status = RtmAddRouteToDest(RtmRegHandle,
                               &RouteHandle,     // Can be NULL if you do not need handle
                               &NetAddress,
                               &RouteInfo,
                               1000,             // Time out route after 1000 ms
                               RouteListHandle1, // Also add the route to this list
                               0,
                               NULL,
                               &ChangeFlags);

    if (Status == NO_ERROR)
    {
        if (ChangeFlags & RTM_ROUTE_CHANGE_NEW)
        {
        ; // A new route has been created
        }
        else
        {
        ; // An existing route is updated
        }

        if (ChangeFlags & RTM_ROUTE_CHANGE_BEST)
        {
        ; // Best route information has changed
        }

        // Release the route handle if you do not need it
        RtmReleaseRoutes(RtmRegHandle, 1, &RouteHandle);
    }

    // Also release the next hop since it is no longer needed 
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHopHandle);
}
```



 

 




