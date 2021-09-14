---
description: Le LSA fournit des fonctions que vous pouvez utiliser pour recevoir une notification en cas de modification de la stratégie sur le système local.
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: Réception des événements de modification de stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33145974ce712f21b338ba35f1571c8f3046c42c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011130"
---
# <a name="receiving-policy-change-events"></a>Réception des événements de modification de stratégie

Le LSA fournit des fonctions que vous pouvez utiliser pour recevoir une notification en cas de modification de la stratégie sur le système local.

Pour recevoir une notification, créez un nouvel objet d’événement en appelant la fonction [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) , puis appelez la fonction [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) . Votre application peut ensuite appeler une fonction Wait telle que [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)ou [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) pour attendre que l’événement se produise. La fonction Wait retourne lorsque l’événement se produit ou lorsque le délai d’attente expire. En règle générale, les événements de notification sont utilisés dans les applications multithread, dans lesquelles un thread attend un événement, tandis que les autres threads continuent le traitement.

Lorsque votre application n’a plus besoin de recevoir des notifications, elle doit appeler [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) , puis appeler [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) pour libérer le handle d’objet d’événement.

L’exemple suivant montre comment une application à thread unique peut recevoir des événements de notification lorsque la stratégie d’audit du système change.


```C++
#include <windows.h>
#include <stdio.h>

void WaitForPolicyChanges()
{
  HANDLE hEvent;
  NTSTATUS ntsResult;
  DWORD dwResult;

  // Create an event object.
  hEvent = CreateEvent( 
    NULL,  // child processes cannot inherit 
    FALSE, // automatically reset event
    FALSE, // start as a nonsignaled event
    NULL   // do not need a name
  );

  // Check that the event was created.
  if (hEvent == NULL) 
  {
    wprintf(L"Event object creation failed: %d\n",GetLastError());
    return;
  }
  // Register to receive auditing policy change notifications.
  ntsResult = LsaRegisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );
  if (STATUS_SUCCESS != ntsResult)
  {
    wprintf(L"LsaRegisterPolicyChangeNotification failed.\n");
    CloseHandle(hEvent);
    return;
  }

  // Wait for the event to be triggered.
  dwResult = WaitForSingleObject( 
    hEvent, // handle to the event object
    300000  // time-out interval, in milliseconds
  );

  // The wait function returned.
  if (dwResult == WAIT_OBJECT_0)
  {  // received the notification signal
    wprintf(L"Notification received.\n");
  } 
  else 
  {  // received a time-out or error
    wprintf(L"Notification was not received.\n");
  }
  // Unregister for notification.
  LsaUnregisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );

  // Free the event handle.
  CloseHandle(hEvent);
}
```



Pour plus d’informations sur les objets d’événement, les fonctions Wait et la synchronisation, consultez [utilisation des objets d’événement](/windows/desktop/Sync/using-event-objects).

 

 
