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
# <a name="using-named-objects"></a>Utilisation d’objets nommés

L’exemple suivant illustre l’utilisation de [noms d’objets](object-names.md) en créant et en ouvrant un mutex nommé.

## <a name="first-process"></a>Premier processus

Le premier processus utilise la fonction [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) pour créer l’objet Mutex. Notez que cette fonction fonctionne, même s’il existe déjà un objet portant le même nom.


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



## <a name="second-process"></a>Deuxième processus

Le deuxième processus utilise la fonction [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) pour ouvrir un handle vers le mutex existant. Cette fonction échoue si un objet mutex portant le nom spécifié n’existe pas. Le paramètre Access demande un accès complet à l’objet mutex, ce qui est nécessaire pour que le handle soit utilisé dans l’une des fonctions Wait.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Noms d’objets](object-names.md)
</dt> <dt>

[Utilisation d’objets mutex](using-mutex-objects.md)
</dt> </dl>

 

 
