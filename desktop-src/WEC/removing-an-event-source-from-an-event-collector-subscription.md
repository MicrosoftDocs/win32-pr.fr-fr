---
title: Suppression d’une source d’événement d’un abonnement initié par le collecteur
description: Vous pouvez supprimer une source d’événement d’un abonnement initié par le collecteur sans supprimer l’intégralité de l’abonnement.
ms.assetid: 6c9e0dbf-59a2-4db9-8fb8-0dbfda5cf38b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303e0a708c2b52225af83475674e5f60d1a8418d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840330"
---
# <a name="removing-an-event-source-from-a-collector-initiated-subscription"></a><span data-ttu-id="9c952-103">Suppression d’une source d’événement d’un abonnement initié par le collecteur</span><span class="sxs-lookup"><span data-stu-id="9c952-103">Removing an Event Source from a Collector Initiated Subscription</span></span>

<span data-ttu-id="9c952-104">Vous pouvez supprimer une source d’événement d’un abonnement initié par le collecteur sans supprimer l’intégralité de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c952-104">You can remove an event source from a collector initiated subscription without deleting the entire subscription.</span></span> <span data-ttu-id="9c952-105">Vous devez connaître l’adresse de la source d’événements que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="9c952-105">You must know the address of the event source that you want to delete.</span></span> <span data-ttu-id="9c952-106">Vous pouvez trouver l’adresse d’une source d’événement qui est associée à un abonnement à l’aide de l’exemple C++ présenté dans [affichage des propriétés d’un abonnement au collecteur d’événements](displaying-the-properties-of-an-event-collector-subscription.md), ou vous pouvez taper la commande suivante à l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="9c952-106">You can find the address of an event source that is associated to a subscription by using the C++ example shown in [Displaying the Properties of an Event Collector Subscription](displaying-the-properties-of-an-event-collector-subscription.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="9c952-107">**wecutil GS** *SubscriptionName*</span><span class="sxs-lookup"><span data-stu-id="9c952-107">**wecutil gs** *SubscriptionName*</span></span>

<span data-ttu-id="9c952-108">Pour répertorier les abonnements en cours sur un ordinateur local, vous pouvez utiliser l’exemple de code C++ présenté dans la [liste des abonnements du collecteur d’événements](listing-event-collector-subscriptions.md), ou vous pouvez taper la commande suivante à l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="9c952-108">To list the current subscriptions on a local computer, you can use the C++ code example shown in [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="9c952-109">**wecutil es**</span><span class="sxs-lookup"><span data-stu-id="9c952-109">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="9c952-110">Vous pouvez utiliser cet exemple pour supprimer une source d’événement d’un abonnement initié par le collecteur, ou vous pouvez taper la commande suivante à l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="9c952-110">You can use this example to remove an event source from a collector initiated subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="9c952-111">**wecutil SS** *SubscriptionName*  \* */ESA : \* \* \* EventSourceAddress* **/res**</span><span class="sxs-lookup"><span data-stu-id="9c952-111">**wecutil ss** *SubscriptionName* \**/esa:\*\*\*EventSourceAddress* **/res**</span></span>
>
> <span data-ttu-id="9c952-112">*EventSourceAddress* peut être localhost pour l’ordinateur local ou un nom de domaine complet pour un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="9c952-112">*EventSourceAddress* can be either localhost for the local computer or a fully qualified domain name for a remote computer.</span></span>

 

<span data-ttu-id="9c952-113">Cet exemple suit une série d’étapes pour supprimer une source d’événement d’un abonnement initié par le collecteur.</span><span class="sxs-lookup"><span data-stu-id="9c952-113">This example follows a series of steps to remove an event source from a collector-initiated subscription.</span></span>

<span data-ttu-id="9c952-114">**Pour supprimer une source d’événement d’un abonnement initié par le collecteur**</span><span class="sxs-lookup"><span data-stu-id="9c952-114">**To remove an event source from a collector-initiated subscription**</span></span>

1.  <span data-ttu-id="9c952-115">Ouvrez l’abonnement existant en fournissant le nom de l’abonnement et les droits d’accès en tant que paramètres à la fonction [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="9c952-115">Open the existing subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="9c952-116">Pour plus d’informations sur les droits d’accès, consultez [**constantes du collecteur d’événements Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9c952-116">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="9c952-117">Récupérez le tableau des sources d’événements de l’abonnement en appelant la fonction [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) .</span><span class="sxs-lookup"><span data-stu-id="9c952-117">Get the event sources array of the subscription by calling the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) function.</span></span> <span data-ttu-id="9c952-118">Pour plus d’informations sur les propriétés d’abonnement qui peuvent être récupérées, consultez l’énumération de l' [**\_ ID de \_ propriété \_ d’abonnement EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .</span><span class="sxs-lookup"><span data-stu-id="9c952-118">For more information about subscription properties that can be retrieved, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="9c952-119">Recherchez la source d’événements spécifiée dans le tableau des sources d’événements de l’abonnement en appelant la fonction [**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) .</span><span class="sxs-lookup"><span data-stu-id="9c952-119">Search for the specified event source in the event sources array of the subscription by calling the [**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) function.</span></span> <span data-ttu-id="9c952-120">La valeur de la propriété **EcSubscriptionEventSourceAddress** sera localhost pour l’ordinateur local ou sera un nom de domaine complet pour un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="9c952-120">The value of the **EcSubscriptionEventSourceAddress** property will be either Localhost for the local computer or will be a fully qualified domain name for a remote computer.</span></span> <span data-ttu-id="9c952-121">Pour plus d’informations sur les propriétés de la source d’événements qui peuvent être récupérées, consultez l’énumération de l' **\_ ID de \_ propriété \_ d’abonnement EC** .</span><span class="sxs-lookup"><span data-stu-id="9c952-121">For more information about event source properties that can be retrieved, see the **EC\_SUBSCRIPTION\_PROPERTY\_ID** enumeration.</span></span>
4.  <span data-ttu-id="9c952-122">Supprimez la source de l’événement de l’abonnement en appelant la fonction [**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) .</span><span class="sxs-lookup"><span data-stu-id="9c952-122">Delete the event source from the subscription by calling the [**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) function.</span></span>
5.  <span data-ttu-id="9c952-123">Enregistrez l’abonnement en appelant la fonction [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .</span><span class="sxs-lookup"><span data-stu-id="9c952-123">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
6.  <span data-ttu-id="9c952-124">Fermez l’abonnement en appelant la fonction [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="9c952-124">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="9c952-125">L’exemple de code C++ suivant montre comment supprimer une source d’événement d’un abonnement à un collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="9c952-125">The following C++ code example shows how to remove an event source from an Event Collector subscription.</span></span>


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Subscription Information
DWORD GetSubscriptionProperty(EC_HANDLE hSubscription,  
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty);
DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD arrayIndex, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProper);



void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost";
    BOOL foundEventSource = false;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD deleteEvent = 0; 
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vProperty = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription(lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS,
        EC_OPEN_EXISTING);

    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to remove an event 
    // source from the subscription.
    dwRetVal = GetSubscriptionProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vProperty);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained.
    if (vProperty->Type != EcVarTypeNull  && 
        vProperty->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vProperty->Type == EcVarTypeNull)? NULL: 
        vProperty->PropertyHandleVal;
    if (!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Search for the specified event source in the event source array.
    for (DWORD I = 0; I < dwEventSourceCount; I++)
    {
        dwRetVal = GetEventSourceProperty(hArray, 
            EcSubscriptionEventSourceAddress, 
            I,
            0,
            buffer,
            vProperty);
        if (ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }

        if (vProperty->StringVal == eventSource)
        {
            foundEventSource = true;
            deleteEvent = I;
            break;
        }
    }

    // Step 4: If the event source was found in the array, remove it.
    if (foundEventSource)
    {
        if (!EcRemoveObjectArrayElement(hArray, deleteEvent))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }
    else
    {
        wprintf(L"Could not remove the event source from the subscription.\n");
        goto Cleanup;
    }

    // Step 5: Save the subscription to finalize the removal of the event source.
    if( !EcSaveSubscription(hSubscription, NULL) )
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 6: Close the subscription.
    Cleanup:
        if (hArray)
            EcClose(hArray);
        if (hSubscription)
            EcClose(hSubscription);

        if (dwRetVal != ERROR_SUCCESS)
        {
            FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
                NULL,
                dwRetVal,
                0,
                (LPWSTR) &lpwszBuffer,
                0,
                NULL);
            
            if (!lpwszBuffer)
            {
                wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." \
                    L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
                return;
            }

            wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n" \
                L"Error Message: %s\n", dwRetVal, lpwszBuffer);

            LocalFree(lpwszBuffer);
        }
}

DWORD GetSubscriptionProperty(EC_HANDLE hSubscription, 
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty)
{
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hSubscription)
    return ERROR_INVALID_PARAMETER;

    // Get the value for the specified property. 
    if (!EcGetSubscriptionProperty(hSubscription,
        propID,
        flags,
        (DWORD) buffer.size(),
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetSubscriptionProperty(hSubscription,
                propID,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}

DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID,
    DWORD arrayIndex,
    DWORD flags,
    std::vector<BYTE>& buffer,
    PEC_VARIANT& vProperty)
{
    UNREFERENCED_PARAMETER(flags);
    UNREFERENCED_PARAMETER(propID);
    
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hArray)
        return ERROR_INVALID_PARAMETER;

    // Obtain the value for the specified property. 
    if (!EcGetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceAddress, 
        arrayIndex,
        0, 
        (DWORD) buffer.size(), 
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetObjectArrayProperty(hArray,
                EcSubscriptionEventSourceAddress,
                arrayIndex,
                0, 
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}
```



## <a name="related-topics"></a><span data-ttu-id="9c952-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c952-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c952-127">Affichage des propriétés d’un abonnement à un collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="9c952-127">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="9c952-128">Liste des abonnements du collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="9c952-128">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="9c952-129">Informations de référence sur le collecteur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="9c952-129">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




