---
description: Le LSA fournit des fonctions que vous pouvez utiliser pour recevoir une notification en cas de modification de la stratégie sur le système local.
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: Réception des événements de modification de stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33145974ce712f21b338ba35f1571c8f3046c42c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515003"
---
# <a name="receiving-policy-change-events"></a><span data-ttu-id="8f104-103">Réception des événements de modification de stratégie</span><span class="sxs-lookup"><span data-stu-id="8f104-103">Receiving Policy Change Events</span></span>

<span data-ttu-id="8f104-104">Le LSA fournit des fonctions que vous pouvez utiliser pour recevoir une notification en cas de modification de la stratégie sur le système local.</span><span class="sxs-lookup"><span data-stu-id="8f104-104">The LSA provides functions you can use to receive notification when there is a change in policy on the local system.</span></span>

<span data-ttu-id="8f104-105">Pour recevoir une notification, créez un nouvel objet d’événement en appelant la fonction [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) , puis appelez la fonction [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) .</span><span class="sxs-lookup"><span data-stu-id="8f104-105">To receive notification, create a new event object by calling the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function, and then call the [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) function.</span></span> <span data-ttu-id="8f104-106">Votre application peut ensuite appeler une fonction Wait telle que [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)ou [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) pour attendre que l’événement se produise.</span><span class="sxs-lookup"><span data-stu-id="8f104-106">Your application can then call a wait function such as [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), or [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) to wait for the event to occur.</span></span> <span data-ttu-id="8f104-107">La fonction Wait retourne lorsque l’événement se produit ou lorsque le délai d’attente expire.</span><span class="sxs-lookup"><span data-stu-id="8f104-107">The wait function returns when the event occurs, or when the time-out period expires.</span></span> <span data-ttu-id="8f104-108">En règle générale, les événements de notification sont utilisés dans les applications multithread, dans lesquelles un thread attend un événement, tandis que les autres threads continuent le traitement.</span><span class="sxs-lookup"><span data-stu-id="8f104-108">Typically, notification events are used in multithreaded applications, in which one thread waits for an event, while other threads continue processing.</span></span>

<span data-ttu-id="8f104-109">Lorsque votre application n’a plus besoin de recevoir des notifications, elle doit appeler [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) , puis appeler [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) pour libérer le handle d’objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="8f104-109">When your application no longer needs to receive notifications, it should call [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) and then call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to free the event object handle.</span></span>

<span data-ttu-id="8f104-110">L’exemple suivant montre comment une application à thread unique peut recevoir des événements de notification lorsque la stratégie d’audit du système change.</span><span class="sxs-lookup"><span data-stu-id="8f104-110">The following example shows how a single-threaded application can receive notification events when the system's auditing policy changes.</span></span>


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



<span data-ttu-id="8f104-111">Pour plus d’informations sur les objets d’événement, les fonctions Wait et la synchronisation, consultez [utilisation des objets d’événement](/windows/desktop/Sync/using-event-objects).</span><span class="sxs-lookup"><span data-stu-id="8f104-111">For more information about event objects, wait functions, and synchronization, see [Using Event Objects](/windows/desktop/Sync/using-event-objects).</span></span>

 

 
