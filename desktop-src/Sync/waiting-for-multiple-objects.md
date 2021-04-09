---
description: L’exemple suivant utilise la fonction CreateEvent pour créer deux objets d’événement et la fonction CreateThread pour créer un thread.
ms.assetid: 0132ac94-b45b-438a-b96a-e77cfe522702
title: En attente de plusieurs objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6fc04d8737b0c404cf6296e1264fa86eb359be6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867385"
---
# <a name="waiting-for-multiple-objects"></a>En attente de plusieurs objets

L’exemple suivant utilise la fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) pour créer deux objets d’événement et la fonction [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) pour créer un thread. Il utilise ensuite la fonction [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) pour attendre que le thread définit l’état de l’un des objets à signaler à l’aide de la fonction [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) .

Pour obtenir un exemple qui attend un seul objet, consultez [utilisation d’objets mutex](using-mutex-objects.md).


```C++
#include <windows.h>
#include <stdio.h>

HANDLE ghEvents[2];

DWORD WINAPI ThreadProc( LPVOID );

int main( void )
{
    HANDLE hThread; 
    DWORD i, dwEvent, dwThreadID; 

    // Create two event objects

    for (i = 0; i < 2; i++) 
    { 
        ghEvents[i] = CreateEvent( 
            NULL,   // default security attributes
            FALSE,  // auto-reset event object
            FALSE,  // initial state is nonsignaled
            NULL);  // unnamed object

        if (ghEvents[i] == NULL) 
        { 
            printf("CreateEvent error: %d\n", GetLastError() ); 
            ExitProcess(0); 
        } 
    } 

    // Create a thread

    hThread = CreateThread( 
                 NULL,         // default security attributes
                 0,            // default stack size
                 (LPTHREAD_START_ROUTINE) ThreadProc, 
                 NULL,         // no thread function arguments
                 0,            // default creation flags
                 &dwThreadID); // receive thread identifier

    if( hThread == NULL )
    {
        printf("CreateThread error: %d\n", GetLastError());
        return 1;
    }

    // Wait for the thread to signal one of the event objects

    dwEvent = WaitForMultipleObjects( 
        2,           // number of objects in array
        ghEvents,     // array of objects
        FALSE,       // wait for any object
        5000);       // five-second wait

    // The return value indicates which event is signaled

    switch (dwEvent) 
    { 
        // ghEvents[0] was signaled
        case WAIT_OBJECT_0 + 0: 
            // TODO: Perform tasks required by this event
            printf("First event was signaled.\n");
            break; 

        // ghEvents[1] was signaled
        case WAIT_OBJECT_0 + 1: 
            // TODO: Perform tasks required by this event
            printf("Second event was signaled.\n");
            break; 

        case WAIT_TIMEOUT:
            printf("Wait timed out.\n");
            break;

        // Return value is invalid.
        default: 
            printf("Wait error: %d\n", GetLastError()); 
            ExitProcess(0); 
    }

    // Close event handles

    for (i = 0; i < 2; i++) 
        CloseHandle(ghEvents[i]); 
    
    return 0;   
}

DWORD WINAPI ThreadProc( LPVOID lpParam )
{

    // lpParam not used in this example
    UNREFERENCED_PARAMETER( lpParam);

    // Set one event to the signaled state

    if ( !SetEvent(ghEvents[0]) ) 
    {
        printf("SetEvent failed (%d)\n", GetLastError());
        return 1;
    }
    return 0;
}
```



 

 
