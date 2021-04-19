---
description: La fonction CreateThread crée un nouveau thread pour un processus.
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: Création de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545088779bdaff665a8079296014535ab244e821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106537016"
---
# <a name="creating-threads"></a>Création de threads

La fonction [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crée un nouveau thread pour un processus. Le thread de création doit spécifier l’adresse de début du code que le nouveau thread doit exécuter. En règle générale, l’adresse de départ est le nom d’une fonction définie dans le code du programme (pour plus d’informations, consultez [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))). Cette fonction accepte un seul paramètre et retourne une valeur **DWORD** . Un processus peut avoir plusieurs threads qui exécutent simultanément la même fonction.

Voici un exemple simple qui montre comment créer un nouveau thread qui exécute la fonction définie localement, `MyThreadFunction` .

Le thread appelant utilise la fonction [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) pour rendre persistante jusqu’à ce que tous les threads de travail soient terminés. Le thread appelant se bloque pendant qu’il attend ; pour continuer le traitement, un thread appelant utilise [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) et attend que chaque thread de travail signale son objet Wait. Notez que, si vous deviez fermer le descripteur d’un thread de travail avant qu’il ne se termine, le thread de travail ne se termine pas. Toutefois, le handle ne peut pas être utilisé dans les appels de fonction suivants.


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>

#define MAX_THREADS 3
#define BUF_SIZE 255

DWORD WINAPI MyThreadFunction( LPVOID lpParam );
void ErrorHandler(LPTSTR lpszFunction);

// Sample custom data structure for threads to use.
// This is passed by void pointer so it can be any data type
// that can be passed using a single void pointer (LPVOID).
typedef struct MyData {
    int val1;
    int val2;
} MYDATA, *PMYDATA;


int _tmain()
{
    PMYDATA pDataArray[MAX_THREADS];
    DWORD   dwThreadIdArray[MAX_THREADS];
    HANDLE  hThreadArray[MAX_THREADS]; 

    // Create MAX_THREADS worker threads.

    for( int i=0; i<MAX_THREADS; i++ )
    {
        // Allocate memory for thread data.

        pDataArray[i] = (PMYDATA) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY,
                sizeof(MYDATA));

        if( pDataArray[i] == NULL )
        {
           // If the array allocation fails, the system is out of memory
           // so there is no point in trying to print an error message.
           // Just terminate execution.
            ExitProcess(2);
        }

        // Generate unique data for each thread to work with.

        pDataArray[i]->val1 = i;
        pDataArray[i]->val2 = i+100;

        // Create the thread to begin execution on its own.

        hThreadArray[i] = CreateThread( 
            NULL,                   // default security attributes
            0,                      // use default stack size  
            MyThreadFunction,       // thread function name
            pDataArray[i],          // argument to thread function 
            0,                      // use default creation flags 
            &dwThreadIdArray[i]);   // returns the thread identifier 


        // Check the return value for success.
        // If CreateThread fails, terminate execution. 
        // This will automatically clean up threads and memory. 

        if (hThreadArray[i] == NULL) 
        {
           ErrorHandler(TEXT("CreateThread"));
           ExitProcess(3);
        }
    } // End of main thread creation loop.

    // Wait until all threads have terminated.

    WaitForMultipleObjects(MAX_THREADS, hThreadArray, TRUE, INFINITE);

    // Close all thread handles and free memory allocations.

    for(int i=0; i<MAX_THREADS; i++)
    {
        CloseHandle(hThreadArray[i]);
        if(pDataArray[i] != NULL)
        {
            HeapFree(GetProcessHeap(), 0, pDataArray[i]);
            pDataArray[i] = NULL;    // Ensure address is not reused.
        }
    }

    return 0;
}


DWORD WINAPI MyThreadFunction( LPVOID lpParam ) 
{ 
    HANDLE hStdout;
    PMYDATA pDataArray;

    TCHAR msgBuf[BUF_SIZE];
    size_t cchStringSize;
    DWORD dwChars;

    // Make sure there is a console to receive output results. 

    hStdout = GetStdHandle(STD_OUTPUT_HANDLE);
    if( hStdout == INVALID_HANDLE_VALUE )
        return 1;

    // Cast the parameter to the correct data type.
    // The pointer is known to be valid because 
    // it was checked for NULL before the thread was created.
 
    pDataArray = (PMYDATA)lpParam;

    // Print the parameter values using thread-safe functions.

    StringCchPrintf(msgBuf, BUF_SIZE, TEXT("Parameters = %d, %d\n"), 
        pDataArray->val1, pDataArray->val2); 
    StringCchLength(msgBuf, BUF_SIZE, &cchStringSize);
    WriteConsole(hStdout, msgBuf, (DWORD)cchStringSize, &dwChars, NULL);

    return 0; 
} 



void ErrorHandler(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code.

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message.

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR) lpMsgBuf) + lstrlen((LPCTSTR) lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR) lpDisplayBuf, TEXT("Error"), MB_OK); 

    // Free error-handling buffer allocations.

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}
```



La `MyThreadFunction` fonction évite l’utilisation de la bibliothèque Runtime C (CRT), car la plupart de ses fonctions ne sont pas thread-safe, en particulier si vous n’utilisez pas le CRT multithread. Si vous souhaitez utiliser le CRT dans une `ThreadProc` fonction, utilisez la fonction **\_ beginthreadex** à la place.

Il est risqué de passer l’adresse d’une variable locale si le thread de création se termine avant le nouveau thread, car le pointeur devient non valide. Au lieu de cela, vous pouvez soit passer un pointeur vers la mémoire allouée dynamiquement, soit faire en sorte que le thread de création attende la fin du nouveau thread. Les données peuvent également être passées du thread de création au nouveau thread à l’aide de variables globales. Avec les variables globales, il est généralement nécessaire de synchroniser l’accès par plusieurs threads. Pour plus d’informations sur la synchronisation, consultez [synchronisation de plusieurs threads](synchronizing-execution-of-multiple-threads.md).

Le thread de création peut utiliser les arguments de [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) pour spécifier les éléments suivants :

-   Attributs de sécurité pour le descripteur du nouveau thread. Ces attributs de sécurité incluent un indicateur d’héritage qui détermine si le handle peut être hérité par les processus enfants. Les attributs de sécurité incluent également un descripteur de sécurité, que le système utilise pour effectuer des vérifications d’accès sur toutes les utilisations suivantes du handle du thread avant d’accorder l’accès.
-   Taille initiale de la pile du nouveau thread. La pile du thread est allouée automatiquement dans l’espace mémoire du processus. le système augmente la pile en fonction des besoins et la libère lorsque le thread se termine. Pour plus d’informations, consultez [taille de pile des threads](thread-stack-size.md).
-   Indicateur de création qui vous permet de créer le thread dans un état suspendu. Lorsqu’il est suspendu, le thread ne s’exécute pas tant que la fonction [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) n’est pas appelée.

Vous pouvez également créer un thread en appelant la fonction [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) . Cette fonction est utilisée par les processus du débogueur pour créer un thread qui s’exécute dans l’espace d’adressage du processus en cours de débogage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Arrêt d’un thread](terminating-a-thread.md)
</dt> </dl>

 

 
