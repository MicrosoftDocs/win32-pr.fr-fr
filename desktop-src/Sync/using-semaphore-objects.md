---
description: L’exemple suivant utilise un objet Semaphore pour limiter le nombre de threads qui peuvent effectuer une tâche particulière.
ms.assetid: 24a5c13c-573a-4fc2-ac19-98188c9eb68a
title: Utilisation d’objets Semaphore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded28014c7e832ab5bdc96d724d57e314d0cc857
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106525314"
---
# <a name="using-semaphore-objects"></a>Utilisation d’objets Semaphore

L’exemple suivant utilise un [objet Semaphore](semaphore-objects.md) pour limiter le nombre de threads qui peuvent effectuer une tâche particulière. Tout d’abord, elle utilise la fonction [**CreateSemaphore,**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) pour créer le sémaphore et pour spécifier les nombres initiaux et maximaux, puis il utilise la fonction [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) pour créer les threads.

Avant qu’un thread ne tente d’exécuter la tâche, il utilise la fonction [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) pour déterminer si le nombre actuel du sémaphore le permet. Le paramètre de délai d’attente de la fonction Wait est défini à zéro, donc la fonction est retournée immédiatement si le sémaphore est à l’état non signalé. **WaitForSingleObject** décrémente le nombre du sémaphore d’une unité.

Quand un thread termine la tâche, il utilise la fonction [**ReleaseSemaphore,**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) pour incrémenter le nombre du sémaphore, ce qui permet à un autre thread en attente d’effectuer la tâche.


```C++
#include <windows.h>
#include <stdio.h>

#define MAX_SEM_COUNT 10
#define THREADCOUNT 12

HANDLE ghSemaphore;

DWORD WINAPI ThreadProc( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a semaphore with initial and max counts of MAX_SEM_COUNT

    ghSemaphore = CreateSemaphore( 
        NULL,           // default security attributes
        MAX_SEM_COUNT,  // initial count
        MAX_SEM_COUNT,  // maximum count
        NULL);          // unnamed semaphore

    if (ghSemaphore == NULL) 
    {
        printf("CreateSemaphore error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) ThreadProc, 
                     NULL,       // no thread function arguments
                     0,          // default creation flags
                     &ThreadID); // receive thread identifier

        if( aThread[i] == NULL )
        {
            printf("CreateThread error: %d\n", GetLastError());
            return 1;
        }
    }

    // Wait for all threads to terminate

    WaitForMultipleObjects(THREADCOUNT, aThread, TRUE, INFINITE);

    // Close thread and semaphore handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghSemaphore);

    return 0;
}

DWORD WINAPI ThreadProc( LPVOID lpParam )
{

    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwWaitResult; 
    BOOL bContinue=TRUE;

    while(bContinue)
    {
        // Try to enter the semaphore gate.

        dwWaitResult = WaitForSingleObject( 
            ghSemaphore,   // handle to semaphore
            0L);           // zero-second time-out interval

        switch (dwWaitResult) 
        { 
            // The semaphore object was signaled.
            case WAIT_OBJECT_0: 
                // TODO: Perform task
                printf("Thread %d: wait succeeded\n", GetCurrentThreadId());
                bContinue=FALSE;            

                // Simulate thread spending time on task
                Sleep(5);

                // Release the semaphore when task is finished

                if (!ReleaseSemaphore( 
                        ghSemaphore,  // handle to semaphore
                        1,            // increase count by one
                        NULL) )       // not interested in previous count
                {
                    printf("ReleaseSemaphore error: %d\n", GetLastError());
                }
                break; 

            // The semaphore was nonsignaled, so a time-out occurred.
            case WAIT_TIMEOUT: 
                printf("Thread %d: wait timed out\n", GetCurrentThreadId());
                break; 
        }
    }
    return TRUE;
}
```



 

 
