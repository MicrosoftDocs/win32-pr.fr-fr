---
title: Suppression d’un abonnement à un collecteur d’événements
description: Vous pouvez supprimer un abonnement à un collecteur d’événements à partir d’un ordinateur local.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9edf2f9dda2b6393ab147d5f58ff8f889952eaeb7f31f82080558697f117f3c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006089"
---
# <a name="deleting-an-event-collector-subscription"></a>Suppression d’un abonnement à un collecteur d’événements

Vous pouvez supprimer un abonnement à un collecteur d’événements à partir d’un ordinateur local. Vous devez connaître le nom de l’abonnement avant de pouvoir le supprimer. Pour plus d’informations sur la façon de répertorier les abonnements en cours sur un ordinateur local, consultez [liste des abonnements du collecteur d’événements](listing-event-collector-subscriptions.md)ou tapez la commande suivante à l’invite de commandes :

**wecutil es**

> [!Note]
>
> Vous pouvez utiliser cet exemple pour supprimer un abonnement à un collecteur d’événements ou vous pouvez taper la commande suivante à l’invite de commandes :
>
> **wecutil** *SubscriptionName* DS

 

Après avoir récupéré le nom de l’abonnement du collecteur d’événements à supprimer, vous pouvez fournir le nom de l’abonnement en tant que paramètre à [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).

L’exemple de code C++ suivant montre comment supprimer un abonnement à un collecteur d’événements.


```C++
#include <windows.h>
#include <EvColl.h>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    DWORD dwRetVal;
    LPWSTR lpSubname = L"MyTestSubscription";

    // Delete the specified Event Collector subscription.
    if (!EcDeleteSubscription(lpSubname, 0))
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
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." 
                L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n"
            L"Error Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liste des abonnements du collecteur d’événements](listing-event-collector-subscriptions.md)
</dt> <dt>

[Windows Référence du collecteur d’événements](windows-event-collector-reference.md)
</dt> </dl>

 

 




