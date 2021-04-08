---
title: Énumérer tous les itinéraires
description: La procédure suivante décrit les étapes utilisées pour énumérer les entités utilisées par l’API RTMv2. L’exemple de code suivant montre comment énumérer tous les itinéraires.
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c927665cab8d4db492d3a2c5f8e9363fc1fe7be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673761"
---
# <a name="enumerate-all-routes"></a>Énumérer tous les itinéraires

La procédure suivante décrit les étapes utilisées pour énumérer les entités utilisées par l’API RTMv2. L’exemple de code suivant montre comment énumérer tous les itinéraires.

**Le processus de base pour chaque énumération est le suivant :**

1.  Démarrez l’énumération en obtenant un handle à partir du gestionnaire de tables de routage. Appelez [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) et [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) pour fournir les critères qui spécifient le type d’informations énumérées. Ce critère comprend, mais n’est pas limité à une plage de destinations, une interface particulière et les vues dans lesquelles les informations résident.
2.  Appelez [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) et [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) une ou plusieurs fois pour récupérer des données jusqu’à ce que le gestionnaire de table de routage retourne l’erreur plus d' \_ \_ \_ éléments. Les données d’itinéraire, de destination et de tronçon suivant sont retournées dans l’ordre des informations d’adresse (et les valeurs de préférence et de mesure, si les itinéraires sont énumérés).
3.  Appelez [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) et [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) lorsque les descripteurs ou structures d’informations associés à l’énumération ne sont plus nécessaires.
4.  Appelez [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) pour libérer le handle d’énumération qui a été retourné lors de la création de l’énumération. Cette fonction est utilisée pour libérer le handle pour tous les types d’énumérations.

> [!Note]  
> Les itinéraires qui sont dans l’état de blocage sont énumérés uniquement lorsqu’un client demande des données de toutes les vues à l’aide du \_ \_ masque de vue RTM \_ Any.

 

L’exemple de code suivant montre comment énumérer tous les itinéraires dans la table de routage.


```C++
MaxHandles = RegnProfile.MaxHandlesInEnum;

RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

// Do a "route enumeration" over the whole table
// by passing a NULL DestHandle in this function.

DestHandle = NULL; // Give a valid handle to enumerate over a particular destination

Status = RtmCreateRouteEnum(RtmRegHandle,
                            DestHandle,
                            RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST,
                            RTM_ENUM_OWN_ROUTES, // Get only your own routes
                            NULL,
                            0,
                            NULL,
                            0,
                            &EnumHandle2);
if (Status == NO_ERROR)
{
    do
    {
        NumHandles = MaxHandles;

        Status = RtmGetEnumRoutes(RtmRegHandle
                                  EnumHandle2,
                                  &NumHandles,
                                  RouteHandles);

        for (k = 0; k < NumHandles; k++)
        {
            wprintf("Route %d: %p\n", l++, RouteHandles[k]);

            // Get route information using the route's handle
            Status = RtmGetRouteInfo(...RouteHandles[k]...);

            if (Status == NO_ERROR)
            {
                // Do whatever you want with the route info
                //...

                // Release the route information once you are done
                RtmReleaseRouteInfo(...);
            }
        }

        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (Status == NO_ERROR)

    // Close the enumeration and release its resources
    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle2);
}
```



 

 




