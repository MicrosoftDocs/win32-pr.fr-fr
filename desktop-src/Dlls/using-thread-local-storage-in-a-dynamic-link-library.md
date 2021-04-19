---
description: Cette section montre l’utilisation d’une fonction de point d’entrée DLL pour configurer un index de stockage local des threads (TLS) afin de fournir un stockage privé pour chaque thread d’un processus multithread.
ms.assetid: a300f223-b513-4a22-a7a4-5d98cf74d77d
title: Utilisation du stockage local des threads dans une bibliothèque de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261ef7482520b4cb6e6c7b630f10ebb456231283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517733"
---
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a>Utilisation du stockage local des threads dans une bibliothèque de Dynamic-Link

Cette section montre l’utilisation d’une fonction de point d’entrée DLL pour configurer un index de stockage local des threads (TLS) afin de fournir un stockage privé pour chaque thread d’un processus multithread.

L’index TLS est stocké dans une variable globale, ce qui le rend disponible pour toutes les fonctions DLL. Cet exemple part du principe que les données globales de la DLL ne sont pas partagées, car l’index TLS n’est pas nécessairement le même pour chaque processus qui charge la DLL.

La fonction de point d’entrée utilise la fonction [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) pour allouer un index TLS chaque fois qu’un processus charge la dll. Chaque thread peut ensuite utiliser cet index pour stocker un pointeur vers son propre bloc de mémoire.

Lorsque la fonction de point d’entrée est appelée avec la \_ valeur d’attachement du processus dll \_ , le code effectue les actions suivantes :

1.  Utilise la fonction [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) pour allouer un index TLS.
2.  Alloue un bloc de mémoire qui doit être utilisé exclusivement par le thread initial du processus.
3.  Utilise l’index TLS dans un appel à la fonction [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) pour stocker l’adresse du bloc de mémoire dans l’emplacement TLS associé à l’index.

Chaque fois que le processus crée un nouveau thread, la fonction de point d’entrée est appelée avec la \_ valeur d’attachement du thread dll \_ . La fonction de point d’entrée alloue ensuite un bloc de mémoire pour le nouveau thread et y stocke un pointeur à l’aide de l’index TLS.

Lorsqu’une fonction requiert l’accès aux données associées à un index TLS, spécifiez l’index dans un appel à la fonction [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) . Cela récupère le contenu de l’emplacement TLS pour le thread appelant, qui, dans ce cas, est un pointeur vers le bloc de mémoire pour les données. Lorsqu’un processus utilise la liaison au moment du chargement avec cette DLL, la fonction de point d’entrée est suffisante pour gérer le stockage local des threads. Des problèmes peuvent se produire avec un processus qui utilise la liaison au moment de l’exécution, car la fonction de point d’entrée n’est pas appelée pour les threads qui existent avant l’appel de la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , donc la mémoire TLS n’est pas allouée pour ces threads. Cet exemple résout ce problème en vérifiant la valeur retournée par la fonction [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) et en allouant de la mémoire si la valeur indique que l’emplacement TLS pour ce thread n’est pas défini.

Lorsque chaque thread n’a plus besoin d’utiliser un index TLS, il doit libérer la mémoire dont le pointeur est stocké dans l’emplacement TLS. Une fois que tous les threads ont terminé d’utiliser un index TLS, utilisez la fonction [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) pour libérer l’index.

Lorsqu’un thread se termine, la fonction de point d’entrée est appelée avec \_ la \_ valeur de détachement de thread dll et la mémoire de ce thread est libérée. Lorsqu’un processus se termine, la fonction de point d’entrée est appelée avec \_ la \_ valeur de détachement de processus dll et la mémoire référencée par le pointeur dans l’index TLS est libérée.


```C++
// The DLL code

#include <windows.h>

static DWORD dwTlsIndex; // address of shared memory
 
// DllMain() is the entry-point function for this DLL. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL, // DLL module handle
    DWORD fdwReason,                    // reason called
    LPVOID lpvReserved)                 // reserved
{ 
    LPVOID lpvData; 
    BOOL fIgnore; 
 
    switch (fdwReason) 
    { 
        // The DLL is loading due to process 
        // initialization or a call to LoadLibrary. 
 
        case DLL_PROCESS_ATTACH: 
 
            // Allocate a TLS index.
 
            if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
                return FALSE; 
 
            // No break: Initialize the index for first thread.
 
        // The attached process creates a new thread. 
 
        case DLL_THREAD_ATTACH: 
 
            // Initialize the TLS index for this thread.
 
            lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
            if (lpvData != NULL) 
                fIgnore = TlsSetValue(dwTlsIndex, lpvData); 
 
            break; 
 
        // The thread of the attached process terminates.
 
        case DLL_THREAD_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            break; 
 
        // DLL unload due to process termination or FreeLibrary. 
 
        case DLL_PROCESS_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            // Release the TLS index.
 
            TlsFree(dwTlsIndex); 
            break; 
 
        default: 
            break; 
    } 
 
    return TRUE; 
    UNREFERENCED_PARAMETER(hinstDLL); 
    UNREFERENCED_PARAMETER(lpvReserved); 
}

// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.

#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif

__declspec(dllexport)
BOOL WINAPI StoreData(DWORD dw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
   {
      lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
      if (lpvData == NULL) 
         return FALSE;
      if (!TlsSetValue(dwTlsIndex, lpvData))
         return FALSE;
   }

   pData = (DWORD *) lpvData; // Cast to my data type.
   // In this example, it is only a pointer to a DWORD
   // but it can be a structure pointer to contain more complicated data.

   (*pData) = dw;
   return TRUE;
}

__declspec(dllexport)
BOOL WINAPI GetData(DWORD *pdw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
      return FALSE;

   pData = (DWORD *) lpvData;
   (*pdw) = (*pData);
   return TRUE;
}
#ifdef __cplusplus
}
#endif
```



Le code suivant illustre l’utilisation des fonctions DLL définies dans l’exemple précédent.


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
#define DLL_NAME TEXT("testdll")

VOID ErrorExit(LPSTR); 

extern "C" BOOL WINAPI StoreData(DWORD dw);
extern "C" BOOL WINAPI GetData(DWORD *pdw);
 
DWORD WINAPI ThreadFunc(VOID) 
{   
   int i;

   if(!StoreData(GetCurrentThreadId()))
      ErrorExit("StoreData error");

   for(i=0; i<THREADCOUNT; i++)
   {
      DWORD dwOut;
      if(!GetData(&dwOut))
         ErrorExit("GetData error");
      if( dwOut != GetCurrentThreadId())
         printf("thread %d: data is incorrect (%d)\n", GetCurrentThreadId(), dwOut);
      else printf("thread %d: data is correct\n", GetCurrentThreadId());
      Sleep(0);
   }
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
   HMODULE hm;
 
// Load the DLL

   hm = LoadLibrary(DLL_NAME);
   if(!hm)
   {
      ErrorExit("DLL failed to load");
   }

// Create multiple threads. 
 
   for (i = 0; i < THREADCOUNT; i++) 
   { 
      hThread[i] = CreateThread(NULL, // default security attributes 
         0,                           // use default stack size 
         (LPTHREAD_START_ROUTINE) ThreadFunc, // thread function 
         NULL,                    // no thread function argument 
         0,                       // use default creation flags 
         &IDThread);              // returns thread identifier 
 
   // Check the return value for success. 
      if (hThread[i] == NULL) 
         ErrorExit("CreateThread error\n"); 
   } 
 
   WaitForMultipleObjects(THREADCOUNT, hThread, TRUE, INFINITE); 

   FreeLibrary(hm);
 
   return 0; 
} 
 
VOID ErrorExit (LPSTR lpszMessage) 
{ 
   fprintf(stderr, "%s\n", lpszMessage); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Données de bibliothèque de liens dynamiques](dynamic-link-library-data.md)
</dt> <dt>

[Utilisation de TLS (Thread Local Storage)](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
