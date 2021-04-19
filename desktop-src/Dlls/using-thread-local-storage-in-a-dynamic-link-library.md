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
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a><span data-ttu-id="0559a-103">Utilisation du stockage local des threads dans une bibliothèque de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="0559a-103">Using Thread Local Storage in a Dynamic-Link Library</span></span>

<span data-ttu-id="0559a-104">Cette section montre l’utilisation d’une fonction de point d’entrée DLL pour configurer un index de stockage local des threads (TLS) afin de fournir un stockage privé pour chaque thread d’un processus multithread.</span><span class="sxs-lookup"><span data-stu-id="0559a-104">This section shows the use of a DLL entry-point function to set up a thread local storage (TLS) index to provide private storage for each thread of a multithreaded process.</span></span>

<span data-ttu-id="0559a-105">L’index TLS est stocké dans une variable globale, ce qui le rend disponible pour toutes les fonctions DLL.</span><span class="sxs-lookup"><span data-stu-id="0559a-105">The TLS index is stored in a global variable, making it available to all of the DLL functions.</span></span> <span data-ttu-id="0559a-106">Cet exemple part du principe que les données globales de la DLL ne sont pas partagées, car l’index TLS n’est pas nécessairement le même pour chaque processus qui charge la DLL.</span><span class="sxs-lookup"><span data-stu-id="0559a-106">This example assumes that the DLL's global data is not shared, because the TLS index is not necessarily the same for each process that loads the DLL.</span></span>

<span data-ttu-id="0559a-107">La fonction de point d’entrée utilise la fonction [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) pour allouer un index TLS chaque fois qu’un processus charge la dll.</span><span class="sxs-lookup"><span data-stu-id="0559a-107">The entry-point function uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index whenever a process loads the DLL.</span></span> <span data-ttu-id="0559a-108">Chaque thread peut ensuite utiliser cet index pour stocker un pointeur vers son propre bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0559a-108">Each thread can then use this index to store a pointer to its own block of memory.</span></span>

<span data-ttu-id="0559a-109">Lorsque la fonction de point d’entrée est appelée avec la \_ valeur d’attachement du processus dll \_ , le code effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0559a-109">When the entry-point function is called with the DLL\_PROCESS\_ATTACH value, the code performs the following actions:</span></span>

1.  <span data-ttu-id="0559a-110">Utilise la fonction [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) pour allouer un index TLS.</span><span class="sxs-lookup"><span data-stu-id="0559a-110">Uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index.</span></span>
2.  <span data-ttu-id="0559a-111">Alloue un bloc de mémoire qui doit être utilisé exclusivement par le thread initial du processus.</span><span class="sxs-lookup"><span data-stu-id="0559a-111">Allocates a block of memory to be used exclusively by the initial thread of the process.</span></span>
3.  <span data-ttu-id="0559a-112">Utilise l’index TLS dans un appel à la fonction [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) pour stocker l’adresse du bloc de mémoire dans l’emplacement TLS associé à l’index.</span><span class="sxs-lookup"><span data-stu-id="0559a-112">Uses the TLS index in a call to the [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) function to store the address of the memory block in the TLS slot associated with the index.</span></span>

<span data-ttu-id="0559a-113">Chaque fois que le processus crée un nouveau thread, la fonction de point d’entrée est appelée avec la \_ valeur d’attachement du thread dll \_ .</span><span class="sxs-lookup"><span data-stu-id="0559a-113">Each time the process creates a new thread, the entry-point function is called with the DLL\_THREAD\_ATTACH value.</span></span> <span data-ttu-id="0559a-114">La fonction de point d’entrée alloue ensuite un bloc de mémoire pour le nouveau thread et y stocke un pointeur à l’aide de l’index TLS.</span><span class="sxs-lookup"><span data-stu-id="0559a-114">The entry-point function then allocates a block of memory for the new thread and stores a pointer to it by using the TLS index.</span></span>

<span data-ttu-id="0559a-115">Lorsqu’une fonction requiert l’accès aux données associées à un index TLS, spécifiez l’index dans un appel à la fonction [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) .</span><span class="sxs-lookup"><span data-stu-id="0559a-115">When a function requires access to the data associated with a TLS index, specify the index in a call to the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function.</span></span> <span data-ttu-id="0559a-116">Cela récupère le contenu de l’emplacement TLS pour le thread appelant, qui, dans ce cas, est un pointeur vers le bloc de mémoire pour les données.</span><span class="sxs-lookup"><span data-stu-id="0559a-116">This retrieves the contents of the TLS slot for the calling thread, which in this case is a pointer to the memory block for the data.</span></span> <span data-ttu-id="0559a-117">Lorsqu’un processus utilise la liaison au moment du chargement avec cette DLL, la fonction de point d’entrée est suffisante pour gérer le stockage local des threads.</span><span class="sxs-lookup"><span data-stu-id="0559a-117">When a process uses load-time linking with this DLL, the entry-point function is sufficient to manage the thread local storage.</span></span> <span data-ttu-id="0559a-118">Des problèmes peuvent se produire avec un processus qui utilise la liaison au moment de l’exécution, car la fonction de point d’entrée n’est pas appelée pour les threads qui existent avant l’appel de la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , donc la mémoire TLS n’est pas allouée pour ces threads.</span><span class="sxs-lookup"><span data-stu-id="0559a-118">Problems can occur with a process that uses run-time linking because the entry-point function is not called for threads that exist before the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is called, so TLS memory is not allocated for these threads.</span></span> <span data-ttu-id="0559a-119">Cet exemple résout ce problème en vérifiant la valeur retournée par la fonction [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) et en allouant de la mémoire si la valeur indique que l’emplacement TLS pour ce thread n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="0559a-119">This example solves this problem by checking the value returned by the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function and allocating memory if the value indicates that the TLS slot for this thread is not set.</span></span>

<span data-ttu-id="0559a-120">Lorsque chaque thread n’a plus besoin d’utiliser un index TLS, il doit libérer la mémoire dont le pointeur est stocké dans l’emplacement TLS.</span><span class="sxs-lookup"><span data-stu-id="0559a-120">When each thread no longer needs to use a TLS index, it must free the memory whose pointer is stored in the TLS slot.</span></span> <span data-ttu-id="0559a-121">Une fois que tous les threads ont terminé d’utiliser un index TLS, utilisez la fonction [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) pour libérer l’index.</span><span class="sxs-lookup"><span data-stu-id="0559a-121">When all threads have finished using a TLS index, use the [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) function to release the index.</span></span>

<span data-ttu-id="0559a-122">Lorsqu’un thread se termine, la fonction de point d’entrée est appelée avec \_ la \_ valeur de détachement de thread dll et la mémoire de ce thread est libérée.</span><span class="sxs-lookup"><span data-stu-id="0559a-122">When a thread terminates, the entry-point function is called with the DLL\_THREAD\_DETACH value and the memory for that thread is freed.</span></span> <span data-ttu-id="0559a-123">Lorsqu’un processus se termine, la fonction de point d’entrée est appelée avec \_ la \_ valeur de détachement de processus dll et la mémoire référencée par le pointeur dans l’index TLS est libérée.</span><span class="sxs-lookup"><span data-stu-id="0559a-123">When a process terminates, the entry-point function is called with the DLL\_PROCESS\_DETACH value and the memory referenced by the pointer in the TLS index is freed.</span></span>


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



<span data-ttu-id="0559a-124">Le code suivant illustre l’utilisation des fonctions DLL définies dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="0559a-124">The following code demonstrates the use of the DLL functions defined in the previous example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0559a-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0559a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0559a-126">Données de bibliothèque de liens dynamiques</span><span class="sxs-lookup"><span data-stu-id="0559a-126">Dynamic-Link Library Data</span></span>](dynamic-link-library-data.md)
</dt> <dt>

[<span data-ttu-id="0559a-127">Utilisation de TLS (Thread Local Storage)</span><span class="sxs-lookup"><span data-stu-id="0559a-127">Using Thread Local Storage</span></span>](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
