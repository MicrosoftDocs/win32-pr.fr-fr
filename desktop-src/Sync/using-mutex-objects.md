---
description: Vous pouvez utiliser un objet mutex pour protéger une ressource partagée de l’accès simultané par plusieurs threads ou processus.
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: Utilisation d’objets mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd68f41319125613e8569e7b343c0b1601a7735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543504"
---
# <a name="using-mutex-objects"></a>Utilisation d’objets mutex

Vous pouvez utiliser un [objet mutex](mutex-objects.md) pour protéger une ressource partagée de l’accès simultané par plusieurs threads ou processus. Chaque thread doit attendre la propriété du mutex avant de pouvoir exécuter le code qui accède à la ressource partagée. Par exemple, si plusieurs threads partagent l’accès à une base de données, les threads peuvent utiliser un objet mutex pour autoriser un seul thread à la fois à écrire dans la base de données.

L’exemple suivant utilise la fonction [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) pour créer un objet mutex et la fonction [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) pour créer des threads de travail.

Quand un thread de ce processus écrit dans la base de données, il demande d’abord la propriété du mutex à l’aide de la fonction [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) . Si le thread obtient la propriété du mutex, il écrit dans la base de données, puis libère sa propriété du mutex à l’aide de la fonction [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) .

Cet exemple utilise la gestion structurée des exceptions pour s’assurer que le thread libère correctement l’objet Mutex. Le bloc de code **\_ \_ finally** est exécuté quelle que soit la façon dont le bloc **\_ \_ try** se termine (sauf si le bloc **\_ \_ try** comprend un appel à la fonction [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ). Cela empêche l’objet mutex d’être abandonné par inadvertance.

Si un mutex est abandonné, le thread qui possédait le mutex ne l’a pas libéré correctement avant de se terminer. Dans ce cas, l’état de la ressource partagée est indéterminé, et continuer à utiliser le mutex peut masquer une erreur potentiellement sérieuse. Certaines applications peuvent tenter de restaurer la ressource dans un état cohérent ; Cet exemple retourne simplement une erreur et cesse d’utiliser le mutex. Pour plus d’informations, consultez la page [objets mutex](mutex-objects.md).


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 2

HANDLE ghMutex; 

DWORD WINAPI WriteToDatabase( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a mutex with no initial owner

    ghMutex = CreateMutex( 
        NULL,              // default security attributes
        FALSE,             // initially not owned
        NULL);             // unnamed mutex

    if (ghMutex == NULL) 
    {
        printf("CreateMutex error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) WriteToDatabase, 
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

    // Close thread and mutex handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghMutex);

    return 0;
}

DWORD WINAPI WriteToDatabase( LPVOID lpParam )
{ 
    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwCount=0, dwWaitResult; 

    // Request ownership of mutex.

    while( dwCount < 20 )
    { 
        dwWaitResult = WaitForSingleObject( 
            ghMutex,    // handle to mutex
            INFINITE);  // no time-out interval
 
        switch (dwWaitResult) 
        {
            // The thread got ownership of the mutex
            case WAIT_OBJECT_0: 
                __try { 
                    // TODO: Write to the database
                    printf("Thread %d writing to database...\n", 
                            GetCurrentThreadId());
                    dwCount++;
                } 

                __finally { 
                    // Release ownership of the mutex object
                    if (! ReleaseMutex(ghMutex)) 
                    { 
                        // Handle error.
                    } 
                } 
                break; 

            // The thread got ownership of an abandoned mutex
            // The database is in an indeterminate state
            case WAIT_ABANDONED: 
                return FALSE; 
        }
    }
    return TRUE; 
}
```



 

 
