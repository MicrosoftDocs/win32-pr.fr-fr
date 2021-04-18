---
title: Utiliser une liste d’itinéraires Client-Specific
description: Les procédures suivantes expliquent les étapes permettant d’utiliser les listes de routage spécifiques au client. L’exemple de code suivant montre comment implémenter la procédure.
ms.assetid: aa9b7b2a-259f-4ce1-afb6-c04875e8ffe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cfa893bda9e850527c7ebe35590dbe2d08a490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512064"
---
# <a name="use-a-client-specific-route-list"></a><span data-ttu-id="43bfe-104">Utiliser une liste d’itinéraires Client-Specific</span><span class="sxs-lookup"><span data-stu-id="43bfe-104">Use a Client-Specific Route List</span></span>

<span data-ttu-id="43bfe-105">Les procédures suivantes expliquent les étapes permettant d’utiliser les listes de routage spécifiques au client.</span><span class="sxs-lookup"><span data-stu-id="43bfe-105">The following procedures outlines the steps to use the client-specific route lists.</span></span> <span data-ttu-id="43bfe-106">L’exemple de code suivant montre comment implémenter la procédure.</span><span class="sxs-lookup"><span data-stu-id="43bfe-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="43bfe-107">**Pour utiliser cette fonctionnalité, un client doit effectuer les étapes suivantes :**</span><span class="sxs-lookup"><span data-stu-id="43bfe-107">**To use this feature, a client should take the following steps**</span></span>

1.  <span data-ttu-id="43bfe-108">Appelez [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) pour obtenir un handle à partir du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="43bfe-108">Call [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) to obtain a handle from the routing table manager.</span></span>
2.  <span data-ttu-id="43bfe-109">Appelez [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) chaque fois que le client doit ajouter un itinéraire à cette liste.</span><span class="sxs-lookup"><span data-stu-id="43bfe-109">Call [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) whenever the client must add a route to this list.</span></span>
3.  <span data-ttu-id="43bfe-110">Lorsque le client n’a plus besoin de la liste, il doit appeler [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) pour supprimer la liste.</span><span class="sxs-lookup"><span data-stu-id="43bfe-110">When the client no longer requires the list, it should call [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) to remove the list.</span></span>

<span data-ttu-id="43bfe-111">**Si le client doit énumérer les itinéraires de la liste, le client doit effectuer les étapes suivantes**</span><span class="sxs-lookup"><span data-stu-id="43bfe-111">**If the client must enumerate the routes on the list, the client should take the following steps**</span></span>

1.  <span data-ttu-id="43bfe-112">Appelez [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) pour obtenir un descripteur d’énumération à partir du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="43bfe-112">Call [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) to obtain an enumeration handle from the routing table manager.</span></span>
2.  <span data-ttu-id="43bfe-113">Appelez [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) pour obtenir les descripteurs des itinéraires de la liste.</span><span class="sxs-lookup"><span data-stu-id="43bfe-113">Call [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) to obtain the handles to the routes in the list.</span></span>
3.  <span data-ttu-id="43bfe-114">Appelez [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) pour libérer les handles lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="43bfe-114">Call [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) to release the handles when no longer required.</span></span>

<span data-ttu-id="43bfe-115">L’exemple de code suivant montre comment créer et utiliser une liste d’itinéraires propre au client.</span><span class="sxs-lookup"><span data-stu-id="43bfe-115">The following sample code shows how to create and use a client-specific route list.</span></span>


```C++
HANDLE RouteListHandle1;
HANDLE RouteListHandle2;

// Create two entity-specific lists to add routes to

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle1);
// Check Status
//...

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle2);
// Check Status
//...

// Assume you have added a bunch of routes
// by calling RtmAddRouteToDest many times
// with 'RouteListHandle1' specified similar to
// Status = RtmAddRouteToDest(RtmRegHandle,
//                            ...
//                            RouteListHandle1,
//                            ...
//                            &ChangeFlags);

// Enumerate routes in RouteListHandle1 list

// Create an enumeration on the route list

Status = RtmCreateRouteListEnum(RtmRegHandle,
                                RouteListHandle1,
                                &EnumHandle);

if (Status == NO_ERROR)
{
        // Allocate space on the top of the stack
        
    MaxHandles = RegnProfile.MaxHandlesInEnum;

    RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

    // Note how the termination condition is different
    // from other enumerations - the call to the function
    // RtmGetListEnumRoutes always returns NO_ERROR
    // Quit when you get fewer handles than requested
    
    do
    {
                // Get next set of routes from the list enumeration
        
        NumHandles = MaxHandles;

        Status = RtmGetListEnumRoutes(RtmRegHandle,
                                      EnumHandle,
                                      &NumHandles,
                                      RouteHandles);

        for (i = 0; i < NumHandles; i++)
        {
            Print("Route Handle %5lu: %p\n", i, RouteHandles[i]);
        }

        // Move all these routes to another route list
        // They are automatically removed from the old one
        
        Status = RtmInsertInRouteList(RtmRegHandle,
                                      RouteListHandle2,
                                      NumHandles,
                                      RouteHandles);
        // Check Status...
        
                // Release the routes that have been enumerated
        
        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (NumHandles == MaxHandles);

    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle);
}

// Destroy all the entity-specific route lists 
// after removing all routes from these lists;
// the routes themselves are not deleted

Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle1);
ASSERT(Status == NO_ERROR);


Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle2);
ASSERT(Status == NO_ERROR);
```



 

 




