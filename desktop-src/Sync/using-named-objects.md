---
description: L’exemple suivant illustre l’utilisation de noms d’objets en créant et en ouvrant un mutex nommé.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Utilisation d’objets nommés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349e3e26f661ca988bc5c5ebbc7b3c6ea622956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538896"
---
# <a name="using-named-objects"></a><span data-ttu-id="39677-103">Utilisation d’objets nommés</span><span class="sxs-lookup"><span data-stu-id="39677-103">Using Named Objects</span></span>

<span data-ttu-id="39677-104">L’exemple suivant illustre l’utilisation de [noms d’objets](object-names.md) en créant et en ouvrant un mutex nommé.</span><span class="sxs-lookup"><span data-stu-id="39677-104">The following example illustrates the use of [object names](object-names.md) by creating and opening a named mutex.</span></span>

## <a name="first-process"></a><span data-ttu-id="39677-105">Premier processus</span><span class="sxs-lookup"><span data-stu-id="39677-105">First Process</span></span>

<span data-ttu-id="39677-106">Le premier processus utilise la fonction [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) pour créer l’objet Mutex.</span><span class="sxs-lookup"><span data-stu-id="39677-106">The first process uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create the mutex object.</span></span> <span data-ttu-id="39677-107">Notez que cette fonction fonctionne, même s’il existe déjà un objet portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="39677-107">Note that this function succeeds even if there is an existing object with the same name.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>

// This process creates the mutex object.

int main(void)
{
    HANDLE hMutex; 

    hMutex = CreateMutex( 
        NULL,                        // default security descriptor
        FALSE,                       // mutex not owned
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("CreateMutex error: %d\n", GetLastError() ); 
    else 
        if ( GetLastError() == ERROR_ALREADY_EXISTS ) 
            printf("CreateMutex opened an existing mutex\n"); 
        else printf("CreateMutex created a new mutex.\n");

    // Keep this process around until the second process is run
    _getch();

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="second-process"></a><span data-ttu-id="39677-108">Deuxième processus</span><span class="sxs-lookup"><span data-stu-id="39677-108">Second Process</span></span>

<span data-ttu-id="39677-109">Le deuxième processus utilise la fonction [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) pour ouvrir un handle vers le mutex existant.</span><span class="sxs-lookup"><span data-stu-id="39677-109">The second process uses the [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) function to open a handle to the existing mutex.</span></span> <span data-ttu-id="39677-110">Cette fonction échoue si un objet mutex portant le nom spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="39677-110">This function fails if a mutex object with the specified name does not exist.</span></span> <span data-ttu-id="39677-111">Le paramètre Access demande un accès complet à l’objet mutex, ce qui est nécessaire pour que le handle soit utilisé dans l’une des fonctions Wait.</span><span class="sxs-lookup"><span data-stu-id="39677-111">The access parameter requests full access to the mutex object, which is necessary for the handle to be used in any of the wait functions.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

// This process opens a handle to a mutex created by another process.

int main(void)
{
    HANDLE hMutex; 

    hMutex = OpenMutex( 
        MUTEX_ALL_ACCESS,            // request full access
        FALSE,                       // handle not inheritable
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("OpenMutex error: %d\n", GetLastError() );
    else printf("OpenMutex successfully opened the mutex.\n");

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="39677-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39677-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39677-113">Noms d’objets</span><span class="sxs-lookup"><span data-stu-id="39677-113">Object Names</span></span>](object-names.md)
</dt> <dt>

[<span data-ttu-id="39677-114">Utilisation d’objets mutex</span><span class="sxs-lookup"><span data-stu-id="39677-114">Using Mutex Objects</span></span>](using-mutex-objects.md)
</dt> </dl>

 

 
