---
description: L’exemple suivant crée une routine de minuterie qui est exécutée par un thread à partir d’une file d’attente de minuteur après un délai de 10 secondes.
ms.assetid: 779156fe-f825-452b-acbe-e2cb189e24d2
title: Utilisation des files d’attente du minuteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13f7afd18a22c42e3af8cffd8b2b148f68b9d99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534679"
---
# <a name="using-timer-queues"></a>Utilisation des files d’attente du minuteur

L’exemple suivant crée une routine de minuterie qui est exécutée par un thread à partir d’une [file d’attente de minuteur](timer-queues.md) après un délai de 10 secondes. Tout d’abord, le code utilise la fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) pour créer un objet d’événement qui est signalé lorsque le thread de la file d’attente du minuteur se termine. Ensuite, il crée une file d’attente du minuteur et un minuteur de la file d’attente, à l’aide des fonctions [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) et [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) , respectivement. Le code utilise la fonction [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) pour déterminer à quel moment la routine de la minuterie est terminée. Enfin, le code appelle [**DeleteTimerQueue**](/windows/desktop/api/WinBase/nf-winbase-deletetimerqueue) pour le nettoyage.

Pour plus d’informations sur la routine du minuteur, consultez [**WaitOrTimerCallback (**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)).


```C++
#include <windows.h>
#include <stdio.h>

HANDLE gDoneEvent;

VOID CALLBACK TimerRoutine(PVOID lpParam, BOOLEAN TimerOrWaitFired)
{
    if (lpParam == NULL)
    {
        printf("TimerRoutine lpParam is NULL\n");
    }
    else
    {
        // lpParam points to the argument; in this case it is an int

        printf("Timer routine called. Parameter is %d.\n", 
                *(int*)lpParam);
        if(TimerOrWaitFired)
        {
            printf("The wait timed out.\n");
        }
        else
        {
            printf("The wait event was signaled.\n");
        }
    }

    SetEvent(gDoneEvent);
}

int main()
{
    HANDLE hTimer = NULL;
    HANDLE hTimerQueue = NULL;
    int arg = 123;

    // Use an event object to track the TimerRoutine execution
    gDoneEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == gDoneEvent)
    {
        printf("CreateEvent failed (%d)\n", GetLastError());
        return 1;
    }

    // Create the timer queue.
    hTimerQueue = CreateTimerQueue();
    if (NULL == hTimerQueue)
    {
        printf("CreateTimerQueue failed (%d)\n", GetLastError());
        return 2;
    }

    // Set a timer to call the timer routine in 10 seconds.
    if (!CreateTimerQueueTimer( &hTimer, hTimerQueue, 
            (WAITORTIMERCALLBACK)TimerRoutine, &arg , 10000, 0, 0))
    {
        printf("CreateTimerQueueTimer failed (%d)\n", GetLastError());
        return 3;
    }

    // TODO: Do other useful work here 

    printf("Call timer routine in 10 seconds...\n");

    // Wait for the timer-queue thread to complete using an event 
    // object. The thread will signal the event at that time.

    if (WaitForSingleObject(gDoneEvent, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());

    CloseHandle(gDoneEvent);

    // Delete all timers in the timer queue.
    if (!DeleteTimerQueue(hTimerQueue))
        printf("DeleteTimerQueue failed (%d)\n", GetLastError());

    return 0;
}
```



 

 
