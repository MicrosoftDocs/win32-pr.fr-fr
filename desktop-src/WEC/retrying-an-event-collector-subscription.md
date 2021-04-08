---
title: Nouvelle tentative d’abonnement au collecteur d’événements
description: Si un problème se produit avec une source d’événement associée à un abonnement du collecteur d’événements, vous pouvez retenter l’abonnement une fois le problème résolu.
ms.assetid: 8a3570af-bde3-40e5-8129-84ec313d853f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0f29d485d36bb6f623cb67bd3e8598c4bb46b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674330"
---
# <a name="retrying-an-event-collector-subscription"></a><span data-ttu-id="46e7b-103">Nouvelle tentative d’abonnement au collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="46e7b-103">Retrying an Event Collector Subscription</span></span>

<span data-ttu-id="46e7b-104">Si un problème se produit avec une source d’événement associée à un abonnement du collecteur d’événements, vous pouvez retenter l’abonnement une fois le problème résolu.</span><span class="sxs-lookup"><span data-stu-id="46e7b-104">If a problem occurs with an event source that is associated to an Event Collector subscription, you can retry the subscription after the problem has been solved.</span></span>

> [!Note]
>
> <span data-ttu-id="46e7b-105">Vous pouvez utiliser cet exemple pour réessayer un abonnement ou vous pouvez taper la commande suivante à l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="46e7b-105">You can use this example to retry a subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="46e7b-106">**wecutil RS** *SubscriptionName*</span><span class="sxs-lookup"><span data-stu-id="46e7b-106">**wecutil rs** *SubscriptionName*</span></span>

 

<span data-ttu-id="46e7b-107">Vous aurez besoin du nom d’un abonnement pour retenter l’opération.</span><span class="sxs-lookup"><span data-stu-id="46e7b-107">You will need the name of a subscription to retry it.</span></span> <span data-ttu-id="46e7b-108">Pour répertorier les noms des abonnements en cours sur un ordinateur local, vous pouvez utiliser l’exemple de code C++ présenté dans la [liste des abonnements du collecteur d’événements](listing-event-collector-subscriptions.md), ou vous pouvez taper la commande suivante à l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="46e7b-108">To list the names of current subscriptions on a local computer, you can use the C++ code example shown in [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="46e7b-109">**wecutil es**</span><span class="sxs-lookup"><span data-stu-id="46e7b-109">**wecutil es**</span></span>

> [!Note]  
> <span data-ttu-id="46e7b-110">Cet exemple montre comment réessayer individuellement chaque source d’événement d’un abonnement initié par le collecteur et comment réessayer un abonnement initié par la source.</span><span class="sxs-lookup"><span data-stu-id="46e7b-110">This example shows how to individually retry each event source of a collector initiated subscription and how to retry a source initiated subscription.</span></span>

 

<span data-ttu-id="46e7b-111">L’exemple de code suivant suit une procédure pour réessayer toutes les sources d’événements d’un abonnement à un collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="46e7b-111">The following code example follows a procedure to retry all of the event sources of an Event Collector subscription.</span></span>

<span data-ttu-id="46e7b-112">**Pour réessayer un abonnement à un collecteur d’événements**</span><span class="sxs-lookup"><span data-stu-id="46e7b-112">**To retry an Event Collector subscription**</span></span>

1.  <span data-ttu-id="46e7b-113">Ouvrez l’abonnement en fournissant le nom de l’abonnement et les droits d’accès en tant que paramètres à la fonction [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="46e7b-113">Open the subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="46e7b-114">Pour plus d’informations sur les droits d’accès, consultez [**constantes du collecteur d’événements Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="46e7b-114">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="46e7b-115">Réessayez la source de l’événement en appelant la fonction **EcRetrySubscription** .</span><span class="sxs-lookup"><span data-stu-id="46e7b-115">Retry the event source by calling the **EcRetrySubscription** function.</span></span>
3.  <span data-ttu-id="46e7b-116">Fermez l’abonnement en appelant la fonction [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="46e7b-116">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="46e7b-117">L’exemple de code C++ suivant montre comment réessayer un abonnement à un collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="46e7b-117">The following C++ code example shows how to retry an Event Collector subscription.</span></span>


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Subscription Information
DWORD GetProperty(EC_HANDLE hSubscription,  
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty);
DWORD GetStatus(LPCWSTR subscriptionName, 
    LPCWSTR eventSource, 
    EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID statusInfoID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vStatus);


void __cdecl wmain()
{
    LPVOID lpwszBuffer;
    DWORD dwRetVal, dwEventSourceCount;
    EC_HANDLE hSubscription;
    PEC_VARIANT vProperty, vEventSources;
    std::vector<BYTE> buffer, eventSourceBuffer;
    LPCWSTR lpSubname = L"SourceInit";

    // Step 1: Open the Event Collector subscription.
    hSubscription = EcOpenSubscription(lpSubname,
        EC_READ_ACCESS,
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Determine if the subscription is source initiated or
    // collector initiated.
    dwRetVal = GetProperty(hSubscription,
        EcSubscriptionType,
        0,
        buffer,
        vProperty);
    if (ERROR_SUCCESS != dwRetVal){
        goto Cleanup;
    }

    if( vProperty->Type != EcVarTypeNull && vProperty->Type != EcVarTypeUInt32)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    if( vProperty->UInt32Val == EcSubscriptionTypeSourceInitiated)
    {
        // Retry the subscription (event source parameter is NULL,
        // so the entire subscription is retried).
        if (!EcRetrySubscription(lpSubname, NULL, 0))
            {
                dwRetVal =  GetLastError();
                goto Cleanup;
            }
        wprintf(L"\nThe subscription was retried.\n");
    }
    else if ( vProperty->UInt32Val == EcSubscriptionTypeCollectorInitiated)
    {
        // Get the event sources array to retry each event source.
        dwRetVal = GetStatus(lpSubname, NULL,
            EcSubscriptionRunTimeStatusEventSources,
            0,
            eventSourceBuffer,
            vEventSources);
        if (ERROR_SUCCESS != dwRetVal){
            goto Cleanup;
        }

        // Ensure that a handle to the event sources array has been obtained.
        if (vEventSources->Type != EcVarTypeNull && 
            vEventSources->Type != (EcVarTypeString | EC_VARIANT_TYPE_ARRAY) )
        {
            dwRetVal = ERROR_INVALID_DATA;
            goto Cleanup;
        }

        dwEventSourceCount = vEventSources->Count;
        
        for (DWORD I = 0; I < dwEventSourceCount ; I++)
        {
            LPCWSTR eventSource = vEventSources->StringArr[I];

            if (!eventSource)
                continue;

            // Retry the event source.
            if (!EcRetrySubscription(lpSubname, eventSource, 0))
            {
                dwRetVal =  GetLastError();
                goto Cleanup;
            }
            
        }
        wprintf(L"\nEach event source was retried.\n");
    }

    Cleanup:
        // Step 5: Close the subscription.
        if(hSubscription)
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

DWORD GetProperty(EC_HANDLE hSubscription,
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

// Get the information for the specified EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
DWORD GetStatus(LPCWSTR subscriptionName, 
    LPCWSTR eventSource, 
    EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID statusInfoID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vStatus)
{
    DWORD dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.clear();
    buffer.resize(sizeof(EC_VARIANT));
    
    if ( !EcGetSubscriptionRunTimeStatus( subscriptionName,
        statusInfoID,
        eventSource,
        flags,
        (DWORD) buffer.size(),
        (PEC_VARIANT) &buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if( ERROR_INSUFFICIENT_BUFFER ==  dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);
            if(!EcGetSubscriptionRunTimeStatus( subscriptionName,
                statusInfoID,
                eventSource,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT) &buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if ( ERROR_SUCCESS == dwRetVal)
    {
        vStatus = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vStatus = NULL;
    }

    return dwRetVal;
}
```



## <a name="related-topics"></a><span data-ttu-id="46e7b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="46e7b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46e7b-119">Liste des abonnements du collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="46e7b-119">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="46e7b-120">Informations de référence sur le collecteur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="46e7b-120">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




