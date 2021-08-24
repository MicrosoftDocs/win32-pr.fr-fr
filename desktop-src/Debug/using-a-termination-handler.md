---
description: L’exemple suivant montre comment un gestionnaire de terminaisons est utilisé pour s’assurer que les ressources sont libérées lorsque l’exécution d’un corps de code protégé se termine.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Utilisation d’un gestionnaire de terminaisons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6fe2d2ba8a7b8443eb164571a42347ce6cfb7e99c44f90da25c6fd57863e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655079"
---
# <a name="using-a-termination-handler"></a>Utilisation d’un gestionnaire de terminaisons

L’exemple suivant montre comment un gestionnaire de terminaisons est utilisé pour s’assurer que les ressources sont libérées lorsque l’exécution d’un corps de code protégé se termine. Dans ce cas, un thread utilise la fonction [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) pour attendre la propriété d’un objet de section critique. Quand le thread a terminé l’exécution du code protégé par la section critique, il doit appeler la fonction [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) pour rendre l’objet de section critique disponible pour d’autres threads. L’utilisation d’un gestionnaire de terminaisons garantit que cela se produira. Pour plus d’informations, consultez [objets de section critique](../sync/critical-section-objects.md).


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



 

 
