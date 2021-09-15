---
title: Utiliser l’état de Hold-Down de l’itinéraire
description: L’exemple de code suivant montre comment marquer une destination pour l’état de blocage et comment créer une énumération de destination qui comprend des itinéraires qui sont dans l’état de blocage.
ms.assetid: bdc97fad-4805-4432-96ca-9225a51c92eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcdff6b05f254b03d5aff30b177135702d64f3db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311573"
---
# <a name="use-the-route-hold-down-state"></a>Utiliser l’état de Hold-Down de l’itinéraire

L’exemple de code suivant montre comment marquer une destination pour l’état de blocage et comment créer une énumération de destination qui comprend des itinéraires qui sont dans l’état de blocage.


```C++
#include <windows.h>

// Macro to allocate a RTM_DEST_INFO on the stack
#define ALLOC_RTM_DEST_INFO(NumViews, NumInfos)
        (PRTM_DEST_INFO) _alloca(RTM_SIZE_OF_DEST_INFO(NumViews) * NumInfos)

void main()
{

// Mark the destination for hold down in Unicast view

Status = RtmHoldDestination(RtmRegHandle,
                            DestHandle,
                            RTM_VIEW_MASK_UCAST,
                            30*1000); // 30 seconds
// Check Status

// When the last route on this destination is deleted,
// it is moved from the ViewInfo's Route to HoldRoute.

// To enumerate all destinations - even the ones with
// just hold down routes, use the following API calls

// Code to enumerate destinations in the table

MaxHandles = RegnProfile.MaxHandlesInEnum;

DestInfos = ALLOC_RTM_DEST_INFO(NumViews, MaxHandles);

DestInfoSize = RTM_SIZE_OF_DEST_INFO(NumViews);

// Enumerate all destinations in the subtree (0 / 0)
// (basically the whole tree; you can
// also achieve this by using RTM_ENUM_START)

RTM_IPV4_MAKE_NET_ADDRESS(&NetAddress,
                          0x00000000,
                          0);

// Create a destination enumeration in views = RTM_VIEW_MASK_ANY.

Status = RtmCreateDestEnum(RtmRegHandle,
                           RTM_VIEW_MASK_ANY, // MUST BE EXACTLY THE SAME AS THIS
                           RTM_ENUM_RANGE,
                           &NetAddress,
                           RTM_BEST_PROTOCOL, // Get best route on each destination
                           &EnumHandle);

if (Status == NO_ERROR)
{
    do
    {
        NumInfos = MaxHandles;

        Status = RtmGetEnumDests(RtmRegHandle
                                 EnumHandle,
                                 &NumInfos,
                                 DestInfos);

        for (i = 0; i < NumInfos; i++)
        {
            DestInfo = (PRTM_DEST_INFO) ((PUCHAR)DestInfos+(i*DestInfoSize));

            // Process the current destination information
            // As RTM_VIEW_MASK_ANY = 0, we have
            // no view information returned in the call
            
            // Get actual DestInfo in the specified views 
            // (Assume that only unicast is specified)
                        
            Status = RtmGetDestInfo(RtmRegHandle,
                                    DestInfo.DestHandle,
                                    RTM_BEST_PROTOCOL,
                                    RTM_VIEW_MASK_UCAST,
                                    &DestInfoActual);

            if (Status == NO_ERROR)
            {
                HoldRoute = DestInfoActual.ViewInfo[0].HoldRoute;
                BestRoute = DestInfoActual.ViewInfo[0].Route;

                // Advertise best unicast route (or the hold down route)

                if (HoldRoute)
                {
                    // HoldRoute exists; Advertise it if hold down protocol
                    ; 
                }

                RtmReleaseDestInfo(RtmRegHandle, &DestInfoActual);
            }

            ...
        }

        RtmReleaseDests(RtmRegHandle, NumInfos, DestInfos);
    }
    while (Status == NO_ERROR)

    // Close the enumeration and release its resources
    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle);
}
```



 

 




