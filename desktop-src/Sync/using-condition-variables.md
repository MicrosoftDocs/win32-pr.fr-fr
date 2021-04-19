---
description: Le code suivant implémente une file d’attente de producteur/consommateur.
ms.assetid: 0f79de15-6ce9-4d89-afb5-b4a2f0cf2fe3
title: Utilisation de variables de condition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70989ca0f62271aa5afabfd60deddaeca2187866
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544270"
---
# <a name="using-condition-variables"></a><span data-ttu-id="3923d-103">Utilisation de variables de condition</span><span class="sxs-lookup"><span data-stu-id="3923d-103">Using Condition Variables</span></span>

<span data-ttu-id="3923d-104">Le code suivant implémente une file d’attente de producteur/consommateur.</span><span class="sxs-lookup"><span data-stu-id="3923d-104">The following code implements a producer/consumer queue.</span></span> <span data-ttu-id="3923d-105">La file d’attente est représentée sous la forme d’une mémoire tampon circulaire délimitée et est protégée par une section critique.</span><span class="sxs-lookup"><span data-stu-id="3923d-105">The queue is represented as a bounded circular buffer, and is protected by a critical section.</span></span> <span data-ttu-id="3923d-106">Le code utilise deux variables de condition : l’une utilisée par les producteurs ( `BufferNotFull` ) et l’autre pour les consommateurs ( `BufferNotEmpty` ).</span><span class="sxs-lookup"><span data-stu-id="3923d-106">The code uses two condition variables: one used by producers (`BufferNotFull`) and one used by consumers (`BufferNotEmpty`).</span></span>

<span data-ttu-id="3923d-107">Le code appelle la fonction [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) pour créer les variables de condition.</span><span class="sxs-lookup"><span data-stu-id="3923d-107">The code calls the [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) function to create the condition variables.</span></span> <span data-ttu-id="3923d-108">Les threads de consommateur appellent la fonction [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs) pour attendre l’ajout d’éléments à la file d’attente et la fonction [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) pour signaler au producteur qu’il est prêt pour un plus grand nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="3923d-108">The consumer threads call the [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs) function to wait for items to be added to the queue and the [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) function to signal the producer that it is ready for more items.</span></span> <span data-ttu-id="3923d-109">Les threads producteurs appellent **SleepConditionVariableCS** pour attendre que le consommateur supprime des éléments de la file d’attente et **WakeConditionVariable** pour signaler au consommateur qu’il y a plus d’éléments dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="3923d-109">The producer threads call **SleepConditionVariableCS** to wait for the consumer to remove items from the queue and **WakeConditionVariable** to signal the consumer that there are more items in the queue.</span></span>

<span data-ttu-id="3923d-110">**Windows Server 2003 et Windows XP :** Les variables de condition ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3923d-110">**Windows Server 2003 and Windows XP:** Condition variables are not supported.</span></span>


```C++
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>

#define BUFFER_SIZE 10
#define PRODUCER_SLEEP_TIME_MS 500
#define CONSUMER_SLEEP_TIME_MS 2000

LONG Buffer[BUFFER_SIZE];
LONG LastItemProduced;
ULONG QueueSize;
ULONG QueueStartOffset;

ULONG TotalItemsProduced;
ULONG TotalItemsConsumed;

CONDITION_VARIABLE BufferNotEmpty;
CONDITION_VARIABLE BufferNotFull;
CRITICAL_SECTION   BufferLock;

BOOL StopRequested;

DWORD WINAPI ProducerThreadProc (PVOID p)
{
    ULONG ProducerId = (ULONG)(ULONG_PTR)p;

    while (true)
    {
        // Produce a new item.

        Sleep (rand() % PRODUCER_SLEEP_TIME_MS);

        ULONG Item = InterlockedIncrement (&LastItemProduced);

        EnterCriticalSection (&BufferLock);

        while (QueueSize == BUFFER_SIZE && StopRequested == FALSE)
        {
            // Buffer is full - sleep so consumers can get items.
            SleepConditionVariableCS (&BufferNotFull, &BufferLock, INFINITE);
        }

        if (StopRequested == TRUE)
        {
            LeaveCriticalSection (&BufferLock);
            break;
        }

        // Insert the item at the end of the queue and increment size.

        Buffer[(QueueStartOffset + QueueSize) % BUFFER_SIZE] = Item;
        QueueSize++;
        TotalItemsProduced++;

        printf ("Producer %u: item %2d, queue size %2u\r\n", ProducerId, Item, QueueSize);

        LeaveCriticalSection (&BufferLock);

        // If a consumer is waiting, wake it.

        WakeConditionVariable (&BufferNotEmpty);
    }

    printf ("Producer %u exiting\r\n", ProducerId);
    return 0;
}

DWORD WINAPI ConsumerThreadProc (PVOID p)
{
    ULONG ConsumerId = (ULONG)(ULONG_PTR)p;

    while (true)
    {
        EnterCriticalSection (&BufferLock);

        while (QueueSize == 0 && StopRequested == FALSE)
        {
            // Buffer is empty - sleep so producers can create items.
            SleepConditionVariableCS (&BufferNotEmpty, &BufferLock, INFINITE);
        }

        if (StopRequested == TRUE && QueueSize == 0)
        {
            LeaveCriticalSection (&BufferLock);
            break;
        }

        // Consume the first available item.

        LONG Item = Buffer[QueueStartOffset];

        QueueSize--;
        QueueStartOffset++;
        TotalItemsConsumed++;

        if (QueueStartOffset == BUFFER_SIZE)
        {
            QueueStartOffset = 0;
        }

        printf ("Consumer %u: item %2d, queue size %2u\r\n", 
            ConsumerId, Item, QueueSize);

        LeaveCriticalSection (&BufferLock);

        // If a producer is waiting, wake it.

        WakeConditionVariable (&BufferNotFull);

        // Simulate processing of the item.

        Sleep (rand() % CONSUMER_SLEEP_TIME_MS);
    }

    printf ("Consumer %u exiting\r\n", ConsumerId);
    return 0;
}

int main ( void )
{
    InitializeConditionVariable (&BufferNotEmpty);
    InitializeConditionVariable (&BufferNotFull);

    InitializeCriticalSection (&BufferLock);

    DWORD id;
    HANDLE hProducer1 = CreateThread (NULL, 0, ProducerThreadProc, (PVOID)1, 0, &id);
    HANDLE hConsumer1 = CreateThread (NULL, 0, ConsumerThreadProc, (PVOID)1, 0, &id);
    HANDLE hConsumer2 = CreateThread (NULL, 0, ConsumerThreadProc, (PVOID)2, 0, &id);

    puts ("Press enter to stop...");
    getchar();

    EnterCriticalSection (&BufferLock);
    StopRequested = TRUE;
    LeaveCriticalSection (&BufferLock);

    WakeAllConditionVariable (&BufferNotFull);
    WakeAllConditionVariable (&BufferNotEmpty);

    WaitForSingleObject (hProducer1, INFINITE);
    WaitForSingleObject (hConsumer1, INFINITE);
    WaitForSingleObject (hConsumer2, INFINITE);

    printf ("TotalItemsProduced: %u, TotalItemsConsumed: %u\r\n", 
        TotalItemsProduced, TotalItemsConsumed);
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="3923d-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3923d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3923d-112">Variables de condition</span><span class="sxs-lookup"><span data-stu-id="3923d-112">Condition Variables</span></span>](condition-variables.md)
</dt> </dl>

 

 
