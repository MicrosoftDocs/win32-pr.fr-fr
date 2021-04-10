---
title: Liste des abonnements du collecteur d’événements
description: Vous pouvez récupérer la liste des noms des abonnements du collecteur d’événements qui sont activés sur un ordinateur local.
ms.assetid: b44fc694-b94a-4fc5-95d1-72afb016ad72
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab030e3f85b1abc0e763c30dfa4208023b2e654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674334"
---
# <a name="listing-event-collector-subscriptions"></a><span data-ttu-id="893c2-103">Liste des abonnements du collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="893c2-103">Listing Event Collector Subscriptions</span></span>

<span data-ttu-id="893c2-104">Vous pouvez récupérer la liste des noms des abonnements du collecteur d’événements qui sont activés sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="893c2-104">You can retrieve a list of names of Event Collector subscriptions that are enabled on a local computer.</span></span> <span data-ttu-id="893c2-105">À l’aide de la fonction [**EcOpenSubscriptionEnum**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum) , vous pouvez obtenir un descripteur d’un énumérateur d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="893c2-105">Using the [**EcOpenSubscriptionEnum**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum) function, you can obtain a handle to a subscription enumerator.</span></span> <span data-ttu-id="893c2-106">Une fois le descripteur créé, la fonction [**EcEnumNextSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription) est utilisée pour répertorier les abonnements sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="893c2-106">After the handle is created, the [**EcEnumNextSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription) function is used to list the subscriptions on the local computer.</span></span>

> [!Note]
>
> <span data-ttu-id="893c2-107">Vous pouvez utiliser l’exemple de code suivant pour récupérer une liste d’abonnements, ou vous pouvez taper la commande suivante à l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="893c2-107">You can use the following code example to retrieve a list of subscriptions or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="893c2-108">**wecutil es**</span><span class="sxs-lookup"><span data-stu-id="893c2-108">**wecutil es**</span></span>

 

<span data-ttu-id="893c2-109">L’exemple de code C++ suivant montre comment répertorier les abonnements du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="893c2-109">The following C++ code example shows how to list the Event Collector subscriptions.</span></span>


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    // Lists the Event Collector subscriptions that are available 
    // on the local computer.
    DWORD dwBufferSizeUsed, dwError = ERROR_SUCCESS;
    BOOL bRetVal = true;
    std::vector<WCHAR> buffer(MAX_PATH);
    EC_HANDLE hEnumerator;
    DWORD dwRetVal;

    // Create a handle to access the subscriptions.
    hEnumerator = EcOpenSubscriptionEnum(NULL);

    if (hEnumerator)
    {
        while (bRetVal)
        {
            // Get the next subscription.
            bRetVal = EcEnumNextSubscription(hEnumerator, 
                (DWORD) buffer.size(),
                (LPWSTR) &buffer[0],
                &dwBufferSizeUsed);
            dwError = GetLastError();

            // If the buffer is not large enough, resize it to accommodate the
            // subscription information.
            if (!bRetVal && ERROR_INSUFFICIENT_BUFFER == dwError)
            {
                dwError = ERROR_SUCCESS;
                buffer.resize(dwBufferSizeUsed);

                bRetVal = EcEnumNextSubscription(hEnumerator,
                    (DWORD) buffer.size(),
                    (LPWSTR) &buffer[0],
                    &dwBufferSizeUsed);
                dwError = GetLastError();
            }

            if (!bRetVal && ERROR_NO_MORE_ITEMS == dwError)
            {
                dwError = ERROR_SUCCESS;
                break;
            }

            if (bRetVal && ERROR_SUCCESS != dwError)
            {
                break;
            }
            
            // Output the subscription name.
            wprintf(L"%s\n", (LPCWSTR) &buffer[0]);    
        }
    }
    else
    {
        dwRetVal = GetLastError();
        LPVOID lpwszBuffer;

        FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
            NULL,
            dwRetVal,
            0,
            (LPWSTR) &lpwszBuffer,
            0,
            NULL);

        if (!lpwszBuffer)
        {
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u. Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\nError Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }

    EcClose(hEnumerator);
}
```



## <a name="related-topics"></a><span data-ttu-id="893c2-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="893c2-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="893c2-111">Informations de référence sur le collecteur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="893c2-111">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




