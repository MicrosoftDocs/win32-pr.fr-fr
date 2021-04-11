---
description: Les applications peuvent utiliser des objets d’événement dans un certain nombre de situations pour notifier un thread en attente de l’occurrence d’un événement.
ms.assetid: f3f455bb-7563-4920-a728-f75fa5854dc9
title: Utilisation d’objets d’événement (synchronisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c0c7ee5f58b8359e989b19ffc9c016dd1a6593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865402"
---
# <a name="using-event-objects-synchronization"></a><span data-ttu-id="2cb0a-103">Utilisation d’objets d’événement (synchronisation)</span><span class="sxs-lookup"><span data-stu-id="2cb0a-103">Using Event Objects (Synchronization)</span></span>

<span data-ttu-id="2cb0a-104">Les applications peuvent utiliser des [objets d’événement](event-objects.md) dans un certain nombre de situations pour notifier un thread en attente de l’occurrence d’un événement.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-104">Applications can use [event objects](event-objects.md) in a number of situations to notify a waiting thread of the occurrence of an event.</span></span> <span data-ttu-id="2cb0a-105">Par exemple, les opérations d’e/s avec chevauchement sur les fichiers, les canaux nommés et les appareils de communication utilisent un objet d’événement pour signaler leur achèvement.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-105">For example, overlapped I/O operations on files, named pipes, and communications devices use an event object to signal their completion.</span></span> <span data-ttu-id="2cb0a-106">Pour plus d’informations sur l’utilisation des objets d’événement dans les opérations d’e/s avec chevauchement, consultez [synchronisation et entrée et sortie avec chevauchement](synchronization-and-overlapped-input-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="2cb0a-106">For more information about the use of event objects in overlapped I/O operations, see [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md).</span></span>

<span data-ttu-id="2cb0a-107">L’exemple suivant utilise des objets d’événement pour empêcher plusieurs threads de lire à partir d’une mémoire tampon partagée pendant qu’un thread principal écrit dans cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-107">The following example uses event objects to prevent several threads from reading from a shared memory buffer while a master thread is writing to that buffer.</span></span> <span data-ttu-id="2cb0a-108">Tout d’abord, le thread principal utilise la fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) pour créer un objet d’événement de réinitialisation manuelle dont l’état initial est non signalé.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-108">First, the master thread uses the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event object whose initial state is nonsignaled.</span></span> <span data-ttu-id="2cb0a-109">Ensuite, il crée plusieurs threads de lecture.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-109">Then it creates several reader threads.</span></span> <span data-ttu-id="2cb0a-110">Le thread principal effectue une opération d’écriture, puis définit l’objet d’événement à l’état signalé une fois l’écriture terminée.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-110">The master thread performs a write operation and then sets the event object to the signaled state when it has finished writing.</span></span>

<span data-ttu-id="2cb0a-111">Avant de commencer une opération de lecture, chaque thread de lecture utilise [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) pour attendre que l’objet d’événement de réinitialisation manuelle soit signalé.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-111">Before starting a read operation, each reader thread uses [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) to wait for the manual-reset event object to be signaled.</span></span> <span data-ttu-id="2cb0a-112">Lorsque **WaitForSingleObject** retourne la valeur, cela indique que le thread principal est prêt à commencer son opération de lecture.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-112">When **WaitForSingleObject** returns, this indicates that the main thread is ready for it to begin its read operation.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 4 

HANDLE ghWriteEvent; 
HANDLE ghThreads[THREADCOUNT];

DWORD WINAPI ThreadProc(LPVOID);

void CreateEventsAndThreads(void) 
{
    int i; 
    DWORD dwThreadID; 

    // Create a manual-reset event object. The write thread sets this
    // object to the signaled state when it finishes writing to a 
    // shared buffer. 

    ghWriteEvent = CreateEvent( 
        NULL,               // default security attributes
        TRUE,               // manual-reset event
        FALSE,              // initial state is nonsignaled
        TEXT("WriteEvent")  // object name
        ); 

    if (ghWriteEvent == NULL) 
    { 
        printf("CreateEvent failed (%d)\n", GetLastError());
        return;
    }

    // Create multiple threads to read from the buffer.

    for(i = 0; i < THREADCOUNT; i++) 
    {
        // TODO: More complex scenarios may require use of a parameter
        //   to the thread procedure, such as an event per thread to  
        //   be used for synchronization.
        ghThreads[i] = CreateThread(
            NULL,              // default security
            0,                 // default stack size
            ThreadProc,        // name of the thread function
            NULL,              // no thread parameters
            0,                 // default startup flags
            &dwThreadID); 

        if (ghThreads[i] == NULL) 
        {
            printf("CreateThread failed (%d)\n", GetLastError());
            return;
        }
    }
}

void WriteToBuffer(VOID) 
{
    // TODO: Write to the shared buffer.
    
    printf("Main thread writing to the shared buffer...\n");

    // Set ghWriteEvent to signaled

    if (! SetEvent(ghWriteEvent) ) 
    {
        printf("SetEvent failed (%d)\n", GetLastError());
        return;
    }
}

void CloseEvents()
{
    // Close all event handles (currently, only one global handle).
    
    CloseHandle(ghWriteEvent);
}

int main( void )
{
    DWORD dwWaitResult;

    // TODO: Create the shared buffer

    // Create events and THREADCOUNT threads to read from the buffer

    CreateEventsAndThreads();

    // At this point, the reader threads have started and are most
    // likely waiting for the global event to be signaled. However, 
    // it is safe to write to the buffer because the event is a 
    // manual-reset event.
    
    WriteToBuffer();

    printf("Main thread waiting for threads to exit...\n");

    // The handle for each thread is signaled when the thread is
    // terminated.
    dwWaitResult = WaitForMultipleObjects(
        THREADCOUNT,   // number of handles in array
        ghThreads,     // array of thread handles
        TRUE,          // wait until all are signaled
        INFINITE);

    switch (dwWaitResult) 
    {
        // All thread objects were signaled
        case WAIT_OBJECT_0: 
            printf("All threads ended, cleaning up for application exit...\n");
            break;

        // An error occurred
        default: 
            printf("WaitForMultipleObjects failed (%d)\n", GetLastError());
            return 1;
    } 
            
    // Close the events to clean up

    CloseEvents();

    return 0;
}

DWORD WINAPI ThreadProc(LPVOID lpParam) 
{
    // lpParam not used in this example.
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwWaitResult;

    printf("Thread %d waiting for write event...\n", GetCurrentThreadId());
    
    dwWaitResult = WaitForSingleObject( 
        ghWriteEvent, // event handle
        INFINITE);    // indefinite wait

    switch (dwWaitResult) 
    {
        // Event object was signaled
        case WAIT_OBJECT_0: 
            //
            // TODO: Read from the shared buffer
            //
            printf("Thread %d reading from buffer\n", 
                   GetCurrentThreadId());
            break; 

        // An error occurred
        default: 
            printf("Wait error (%d)\n", GetLastError()); 
            return 0; 
    }

    // Now that we are done reading the buffer, we could use another
    // event to signal that this thread is no longer reading. This
    // example simply uses the thread handle for synchronization (the
    // handle is signaled when the thread terminates.)

    printf("Thread %d exiting\n", GetCurrentThreadId());
    return 1;
}

```



 

 
