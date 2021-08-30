---
title: Mettre à jour un itinéraire sur place à l’aide de RtmUpdateAndUnlockRoute
description: La procédure suivante décrit les étapes utilisées pour mettre à jour un itinéraire sur place. L’exemple de code suivant montre comment implémenter la procédure.
ms.assetid: 3598a28f-8ade-4b3f-9d31-4f2c84df2dd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95429383b3c13bfb0a02282425c004f77205ba494ac4026c8b066db0726b9966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101719"
---
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a>Mettre à jour un itinéraire sur place à l’aide de RtmUpdateAndUnlockRoute

La procédure suivante décrit les étapes utilisées pour mettre à jour un itinéraire sur place. L’exemple de code suivant montre comment implémenter la procédure.

**Pour mettre à jour un itinéraire sur place, le client doit effectuer les étapes suivantes**

1.  Verrouillez l’itinéraire en appelant [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute). Actuellement, cette fonction verrouille réellement la destination de l’itinéraire. Le gestionnaire de tables de routage retourne un pointeur vers l’itinéraire.
2.  Utilisez le pointeur vers la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) du gestionnaire de tables de routage, obtenue à l’étape 1, pour apporter les modifications nécessaires à l’itinéraire. Seuls certains membres de la structure d' **\_ \_ informations d’itinéraire RTM** peuvent être modifiés lors de la mise à jour sur place. Ces membres sont les suivants : **voisin**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews** et **NextHopsList**.
    > [!Note]  
    > Si le client ajoute des informations aux membres **voisins** ou **NextHopsList** , le client doit appeler [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) pour incrémenter explicitement le nombre de références que le gestionnaire de tables de routage conserve sur l’objet tronçon suivant. De même, si le client supprime des informations du membre **NextHopsList** , le client doit appeler [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) pour décrémenter le décompte de références.

     

3.  Appelez [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) pour informer le gestionnaire de table de routage qu’une modification a eu lieu. Le gestionnaire de table de routage valide les modifications, met à jour la destination pour refléter les nouvelles informations, puis déverrouille l’itinéraire.

L’exemple de code suivant montre comment mettre à jour un itinéraire directement à l’aide d’un pointeur vers les informations d’itinéraire réelles dans la table de routage.


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



 

 




