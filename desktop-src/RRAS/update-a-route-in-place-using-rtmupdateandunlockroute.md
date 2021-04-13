---
title: Mettre à jour un itinéraire sur place à l’aide de RtmUpdateAndUnlockRoute
description: La procédure suivante décrit les étapes utilisées pour mettre à jour un itinéraire sur place. L’exemple de code suivant montre comment implémenter la procédure.
ms.assetid: 3598a28f-8ade-4b3f-9d31-4f2c84df2dd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb79b86645d77f0ee44ffd06b8ef6f403dbd8ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380109"
---
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="52b36-104">Mettre à jour un itinéraire sur place à l’aide de RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="52b36-104">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="52b36-105">La procédure suivante décrit les étapes utilisées pour mettre à jour un itinéraire sur place.</span><span class="sxs-lookup"><span data-stu-id="52b36-105">The following procedure outlines the steps used to update a route in place.</span></span> <span data-ttu-id="52b36-106">L’exemple de code suivant montre comment implémenter la procédure.</span><span class="sxs-lookup"><span data-stu-id="52b36-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="52b36-107">**Pour mettre à jour un itinéraire sur place, le client doit effectuer les étapes suivantes**</span><span class="sxs-lookup"><span data-stu-id="52b36-107">**To update a route in place, the client should take the following steps**</span></span>

1.  <span data-ttu-id="52b36-108">Verrouillez l’itinéraire en appelant [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span><span class="sxs-lookup"><span data-stu-id="52b36-108">Lock the route by calling [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span></span> <span data-ttu-id="52b36-109">Actuellement, cette fonction verrouille réellement la destination de l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="52b36-109">Currently, this function actually locks the route's destination.</span></span> <span data-ttu-id="52b36-110">Le gestionnaire de tables de routage retourne un pointeur vers l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="52b36-110">The routing table manager returns a pointer to the route.</span></span>
2.  <span data-ttu-id="52b36-111">Utilisez le pointeur vers la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) du gestionnaire de tables de routage, obtenue à l’étape 1, pour apporter les modifications nécessaires à l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="52b36-111">Use the pointer to the routing table manager's [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure, obtained in step 1, to make the necessary changes to the route.</span></span> <span data-ttu-id="52b36-112">Seuls certains membres de la structure d' **\_ \_ informations d’itinéraire RTM** peuvent être modifiés lors de la mise à jour sur place.</span><span class="sxs-lookup"><span data-stu-id="52b36-112">Only certain members of the **RTM\_ROUTE\_INFO** structure can be modified when updating in place.</span></span> <span data-ttu-id="52b36-113">Ces membres sont les suivants : **voisin**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews** et **NextHopsList**.</span><span class="sxs-lookup"><span data-stu-id="52b36-113">These members are: **Neighbour**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews**, and **NextHopsList**.</span></span>
    > [!Note]  
    > <span data-ttu-id="52b36-114">Si le client ajoute des informations aux membres **voisins** ou **NextHopsList** , le client doit appeler [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) pour incrémenter explicitement le nombre de références que le gestionnaire de tables de routage conserve sur l’objet tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="52b36-114">If the client adds information to either the **Neighbour** or **NextHopsList** members, the client must call [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) to explicitly increment the reference count that the routing table manager keeps on the next-hop object.</span></span> <span data-ttu-id="52b36-115">De même, si le client supprime des informations du membre **NextHopsList** , le client doit appeler [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) pour décrémenter le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="52b36-115">Similarly, if the client removes information from the **NextHopsList** member, the client must call [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) to decrement the reference count.</span></span>

     

3.  <span data-ttu-id="52b36-116">Appelez [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) pour informer le gestionnaire de table de routage qu’une modification a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="52b36-116">Call [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) to notify the routing table manager that a change has taken place.</span></span> <span data-ttu-id="52b36-117">Le gestionnaire de table de routage valide les modifications, met à jour la destination pour refléter les nouvelles informations, puis déverrouille l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="52b36-117">The routing table manager commits the changes, updates the destination to reflect the new information, and then unlocks the route.</span></span>

<span data-ttu-id="52b36-118">L’exemple de code suivant montre comment mettre à jour un itinéraire directement à l’aide d’un pointeur vers les informations d’itinéraire réelles dans la table de routage.</span><span class="sxs-lookup"><span data-stu-id="52b36-118">The following sample code shows how to update a route directly, using a pointer to the actual route information in the routing table.</span></span>


```C++
Status = RtmLockRoute(RtmRegHandle,
                      RouteHandle,
                      TRUE,
                      TRUE,
                      &RoutePointer);

if (Status == NO_ERROR)
{
        // Update route parameters in place (i.e., directly on 
// the routing table manager's copy)
    
    // Update the metric and views of the route
    RoutePointer->PrefInfo.Metric = 16;

    // Change the views so that the route belongs to only the multicast view
    RoutePointer->BelongsToViews = RTM_VIEW_MASK_MCAST;

    // Set the entity-specific information to X
    RoutePointer->EntitySpecificInfo = X;

    // Note that the following manipulation of
    // next-hop references is not needed when
    // using RtmAddRouteToDest, as it is done
    // by the routing table manager automatically
    
    // Change next hop from NextHop1 to NextHop2
    NextHop1 = RoutePointer->NextHopsList.NextHop[0];

    // Explicitly dereference the old next hop
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHop1);

    RoutePointer->NextHopsList.NextHop[0] = NextHop2;

    // Explicitly reference next hop being added
    RtmReferenceHandles(RtmRegHandle, 1, &NextHop2);

    // Call the routing table manager to indicate that route information
    // has changed, and that its position might
    // have to be rearranged and the corresponding destination
    // needs to be updated to reflect this change.
    
    Status = RtmUpdateAndUnlockRoute(RtmRegHandle,
                                     RouteHandle,
                                     INFINITE, // Keep forever
                                     NULL,
                                     0,
                                     NULL,
                                     &ChangeFlags);
    ASSERT(Status == NO_ERROR);
}
```



 

 




