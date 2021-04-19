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
# <a name="using-mutex-objects"></a><span data-ttu-id="602ab-103">Utilisation d’objets mutex</span><span class="sxs-lookup"><span data-stu-id="602ab-103">Using Mutex Objects</span></span>

<span data-ttu-id="602ab-104">Vous pouvez utiliser un [objet mutex](mutex-objects.md) pour protéger une ressource partagée de l’accès simultané par plusieurs threads ou processus.</span><span class="sxs-lookup"><span data-stu-id="602ab-104">You can use a [mutex object](mutex-objects.md) to protect a shared resource from simultaneous access by multiple threads or processes.</span></span> <span data-ttu-id="602ab-105">Chaque thread doit attendre la propriété du mutex avant de pouvoir exécuter le code qui accède à la ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="602ab-105">Each thread must wait for ownership of the mutex before it can execute the code that accesses the shared resource.</span></span> <span data-ttu-id="602ab-106">Par exemple, si plusieurs threads partagent l’accès à une base de données, les threads peuvent utiliser un objet mutex pour autoriser un seul thread à la fois à écrire dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="602ab-106">For example, if several threads share access to a database, the threads can use a mutex object to permit only one thread at a time to write to the database.</span></span>

<span data-ttu-id="602ab-107">L’exemple suivant utilise la fonction [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) pour créer un objet mutex et la fonction [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) pour créer des threads de travail.</span><span class="sxs-lookup"><span data-stu-id="602ab-107">The following example uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create a mutex object and the [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function to create worker threads.</span></span>

<span data-ttu-id="602ab-108">Quand un thread de ce processus écrit dans la base de données, il demande d’abord la propriété du mutex à l’aide de la fonction [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="602ab-108">When a thread of this process writes to the database, it first requests ownership of the mutex using the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function.</span></span> <span data-ttu-id="602ab-109">Si le thread obtient la propriété du mutex, il écrit dans la base de données, puis libère sa propriété du mutex à l’aide de la fonction [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) .</span><span class="sxs-lookup"><span data-stu-id="602ab-109">If the thread obtains ownership of the mutex, it writes to the database and then releases its ownership of the mutex using the [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) function.</span></span>

<span data-ttu-id="602ab-110">Cet exemple utilise la gestion structurée des exceptions pour s’assurer que le thread libère correctement l’objet Mutex.</span><span class="sxs-lookup"><span data-stu-id="602ab-110">This example uses structured exception handling to ensure that the thread properly releases the mutex object.</span></span> <span data-ttu-id="602ab-111">Le bloc de code **\_ \_ finally** est exécuté quelle que soit la façon dont le bloc **\_ \_ try** se termine (sauf si le bloc **\_ \_ try** comprend un appel à la fonction [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ).</span><span class="sxs-lookup"><span data-stu-id="602ab-111">The **\_\_finally** block of code is executed no matter how the **\_\_try** block terminates (unless the **\_\_try** block includes a call to the [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) function).</span></span> <span data-ttu-id="602ab-112">Cela empêche l’objet mutex d’être abandonné par inadvertance.</span><span class="sxs-lookup"><span data-stu-id="602ab-112">This prevents the mutex object from being abandoned inadvertently.</span></span>

<span data-ttu-id="602ab-113">Si un mutex est abandonné, le thread qui possédait le mutex ne l’a pas libéré correctement avant de se terminer.</span><span class="sxs-lookup"><span data-stu-id="602ab-113">If a mutex is abandoned, the thread that owned the mutex did not properly release it before terminating.</span></span> <span data-ttu-id="602ab-114">Dans ce cas, l’état de la ressource partagée est indéterminé, et continuer à utiliser le mutex peut masquer une erreur potentiellement sérieuse.</span><span class="sxs-lookup"><span data-stu-id="602ab-114">In this case, the status of the shared resource is indeterminate, and continuing to use the mutex can obscure a potentially serious error.</span></span> <span data-ttu-id="602ab-115">Certaines applications peuvent tenter de restaurer la ressource dans un état cohérent ; Cet exemple retourne simplement une erreur et cesse d’utiliser le mutex.</span><span class="sxs-lookup"><span data-stu-id="602ab-115">Some applications might attempt to restore the resource to a consistent state; this example simply returns an error and stops using the mutex.</span></span> <span data-ttu-id="602ab-116">Pour plus d’informations, consultez la page [objets mutex](mutex-objects.md).</span><span class="sxs-lookup"><span data-stu-id="602ab-116">For more information, see [Mutex Objects](mutex-objects.md).</span></span>


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



 

 
