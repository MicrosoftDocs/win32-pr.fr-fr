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
# <a name="enumerate-all-routes"></a><span data-ttu-id="fab68-104">Énumérer tous les itinéraires</span><span class="sxs-lookup"><span data-stu-id="fab68-104">Enumerate All Routes</span></span>

<span data-ttu-id="fab68-105">La procédure suivante décrit les étapes utilisées pour énumérer les entités utilisées par l’API RTMv2.</span><span class="sxs-lookup"><span data-stu-id="fab68-105">The following procedure outlines the steps used to enumerate any of the entities used by the RTMv2 API.</span></span> <span data-ttu-id="fab68-106">L’exemple de code suivant montre comment énumérer tous les itinéraires.</span><span class="sxs-lookup"><span data-stu-id="fab68-106">The sample code that follows shows how to enumerate all routes.</span></span>

<span data-ttu-id="fab68-107">**Le processus de base pour chaque énumération est le suivant :**</span><span class="sxs-lookup"><span data-stu-id="fab68-107">**The basic process for each enumeration is as follows**</span></span>

1.  <span data-ttu-id="fab68-108">Démarrez l’énumération en obtenant un handle à partir du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="fab68-108">Start the enumeration by obtaining a handle from the routing table manager.</span></span> <span data-ttu-id="fab68-109">Appelez [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) et [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) pour fournir les critères qui spécifient le type d’informations énumérées.</span><span class="sxs-lookup"><span data-stu-id="fab68-109">Call [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) and [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) to supply the criteria that specifies the kind of information being enumerated.</span></span> <span data-ttu-id="fab68-110">Ce critère comprend, mais n’est pas limité à une plage de destinations, une interface particulière et les vues dans lesquelles les informations résident.</span><span class="sxs-lookup"><span data-stu-id="fab68-110">This criteria includes, but is not limited to a range of destinations, a particular interface, and the views in which the information resides.</span></span>
2.  <span data-ttu-id="fab68-111">Appelez [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) et [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) une ou plusieurs fois pour récupérer des données jusqu’à ce que le gestionnaire de table de routage retourne l’erreur plus d' \_ \_ \_ éléments.</span><span class="sxs-lookup"><span data-stu-id="fab68-111">Call [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) and [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) one or more times to retrieve data until the routing table manager returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="fab68-112">Les données d’itinéraire, de destination et de tronçon suivant sont retournées dans l’ordre des informations d’adresse (et les valeurs de préférence et de mesure, si les itinéraires sont énumérés).</span><span class="sxs-lookup"><span data-stu-id="fab68-112">The route, destination, and next-hop data is returned in order of the address information (and the preference and metric values, if routes are being enumerated).</span></span>
3.  <span data-ttu-id="fab68-113">Appelez [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) et [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) lorsque les descripteurs ou structures d’informations associés à l’énumération ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="fab68-113">Call [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) and [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) when the handles or information structures associated with the enumeration are no longer required.</span></span>
4.  <span data-ttu-id="fab68-114">Appelez [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) pour libérer le handle d’énumération qui a été retourné lors de la création de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="fab68-114">Call [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) to release the enumeration handle that was returned when the enumeration was created.</span></span> <span data-ttu-id="fab68-115">Cette fonction est utilisée pour libérer le handle pour tous les types d’énumérations.</span><span class="sxs-lookup"><span data-stu-id="fab68-115">This function is used to release the handle for all types of enumerations.</span></span>

> [!Note]  
> <span data-ttu-id="fab68-116">Les itinéraires qui sont dans l’état de blocage sont énumérés uniquement lorsqu’un client demande des données de toutes les vues à l’aide du \_ \_ masque de vue RTM \_ Any.</span><span class="sxs-lookup"><span data-stu-id="fab68-116">Routes that are in the hold-down state are only enumerated when a client requests data from all views using RTM\_VIEW\_MASK\_ANY.</span></span>

 

<span data-ttu-id="fab68-117">L’exemple de code suivant montre comment énumérer tous les itinéraires dans la table de routage.</span><span class="sxs-lookup"><span data-stu-id="fab68-117">The following sample code shows how to enumerate all routes in the routing table.</span></span>


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



 

 




