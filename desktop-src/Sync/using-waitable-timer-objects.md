---
description: L’exemple suivant crée une minuterie qui est signalée après un délai de 10 secondes.
ms.assetid: 3c84c2ad-6bac-4f14-a633-51d4529314af
title: Utilisation d’objets Timer Waitables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a23b0d9f6ab74df325be81eb9236bffe6a0c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536187"
---
# <a name="using-waitable-timer-objects"></a>Utilisation d’objets Timer Waitables

L’exemple suivant crée une minuterie qui est signalée après un délai de 10 secondes. Tout d’abord, le code utilise la fonction [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) pour créer un [objet de minuteur](waitable-timer-objects.md)qui est attendu. Elle utilise ensuite la fonction [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) pour définir la minuterie. Le code utilise la fonction [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) pour déterminer quand la minuterie a été signalée.


```C++
#include <windows.h>
#include <stdio.h>

int main()
{
    HANDLE hTimer = NULL;
    LARGE_INTEGER liDueTime;

    liDueTime.QuadPart = -100000000LL;

    // Create an unnamed waitable timer.
    hTimer = CreateWaitableTimer(NULL, TRUE, NULL);
    if (NULL == hTimer)
    {
        printf("CreateWaitableTimer failed (%d)\n", GetLastError());
        return 1;
    }

    printf("Waiting for 10 seconds...\n");

    // Set a timer to wait for 10 seconds.
    if (!SetWaitableTimer(hTimer, &liDueTime, 0, NULL, NULL, 0))
    {
        printf("SetWaitableTimer failed (%d)\n", GetLastError());
        return 2;
    }

    // Wait for the timer.

    if (WaitForSingleObject(hTimer, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());
    else printf("Timer was signaled.\n");

    return 0;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de minuteries Waitables avec un appel de procédure asynchrone](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
