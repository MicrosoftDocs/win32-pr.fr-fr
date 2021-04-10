---
description: L’exemple suivant montre comment un gestionnaire de terminaisons est utilisé pour s’assurer que les ressources sont libérées lorsque l’exécution d’un corps de code protégé se termine.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Utilisation d’un gestionnaire de terminaisons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbe73eda8533ed5805159d5386b69daa4d03194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950621"
---
# <a name="using-a-termination-handler"></a><span data-ttu-id="3694a-103">Utilisation d’un gestionnaire de terminaisons</span><span class="sxs-lookup"><span data-stu-id="3694a-103">Using a Termination Handler</span></span>

<span data-ttu-id="3694a-104">L’exemple suivant montre comment un gestionnaire de terminaisons est utilisé pour s’assurer que les ressources sont libérées lorsque l’exécution d’un corps de code protégé se termine.</span><span class="sxs-lookup"><span data-stu-id="3694a-104">The following example shows how a termination handler is used to ensure that resources are released when execution of a guarded body of code terminates.</span></span> <span data-ttu-id="3694a-105">Dans ce cas, un thread utilise la fonction [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) pour attendre la propriété d’un objet de section critique.</span><span class="sxs-lookup"><span data-stu-id="3694a-105">In this case, a thread uses the [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) function to wait for ownership of a critical section object.</span></span> <span data-ttu-id="3694a-106">Quand le thread a terminé l’exécution du code protégé par la section critique, il doit appeler la fonction [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) pour rendre l’objet de section critique disponible pour d’autres threads.</span><span class="sxs-lookup"><span data-stu-id="3694a-106">When the thread is finished executing the code that is protected by the critical section, it must call the [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) function to make the critical section object available to other threads.</span></span> <span data-ttu-id="3694a-107">L’utilisation d’un gestionnaire de terminaisons garantit que cela se produira.</span><span class="sxs-lookup"><span data-stu-id="3694a-107">Using a termination handler guarantees that this will happen.</span></span> <span data-ttu-id="3694a-108">Pour plus d’informations, consultez [objets de section critique](../sync/critical-section-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3694a-108">For more information, see [critical section objects](../sync/critical-section-objects.md).</span></span>


```C++
LPTSTR lpBuffer = NULL; 
CRITICAL_SECTION CriticalSection; 

// EnterCriticalSection synchronizes code with other threads. 
EnterCriticalSection(&CriticalSection); 
 
__try 
{ 
    // Perform a task that may cause an exception. 
    lpBuffer = (LPTSTR) LocalAlloc(LPTR, 10); 
    StringCchCopy(lpBuffer, 10, TEXT("Hello"));

    _tprintf(TEXT("%s\n"),lpBuffer); 
    LocalFree(lpBuffer); 
} 
__finally 
{ 
    // LeaveCriticalSection is called even if an exception occurred. 
    LeaveCriticalSection(&CriticalSection); 
}
```



 

 
