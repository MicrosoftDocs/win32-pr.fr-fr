---
description: Le stockage local des threads (TLS) permet à plusieurs threads du même processus d’utiliser un index alloué par la fonction TlsAlloc pour stocker et récupérer une valeur locale du thread.
ms.assetid: b7f5a206-a827-4b6b-86f6-5e3aea1246b7
title: Utilisation de TLS (Thread Local Storage)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdac1306a4a2da10e6a24ba2e1b2444f6215fdac39be7b41cc6850c1e5a683d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127989"
---
# <a name="using-thread-local-storage"></a>Utilisation de TLS (Thread Local Storage)

Le [stockage local des threads](thread-local-storage.md) (TLS) permet à plusieurs threads du même processus d’utiliser un index alloué par la fonction [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) pour stocker et récupérer une valeur locale du thread. Dans cet exemple, un index est alloué au démarrage du processus. Lorsque chaque thread démarre, il alloue un bloc de mémoire dynamique et stocke un pointeur vers cette mémoire dans l’emplacement TLS à l’aide de la fonction [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) . La fonction CommonFunc utilise la fonction [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) pour accéder aux données associées à l’index local du thread appelant. Avant que chaque thread se termine, il libère sa mémoire dynamique. Avant que le processus se termine, il appelle [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) pour libérer l’index.


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
DWORD dwTlsIndex; 
 
VOID ErrorExit (LPCSTR message);
 
VOID CommonFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Retrieve a data pointer for the current thread. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if ((lpvData == 0) && (GetLastError() != ERROR_SUCCESS)) 
      ErrorExit("TlsGetValue error"); 
 
// Use the data stored for the current thread. 
 
   printf("common: thread %d: lpvData=%lx\n", 
      GetCurrentThreadId(), lpvData); 
 
   Sleep(5000); 
} 
 
DWORD WINAPI ThreadFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Initialize the TLS index for this thread. 
 
   lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
   if (! TlsSetValue(dwTlsIndex, lpvData)) 
      ErrorExit("TlsSetValue error"); 
 
   printf("thread %d: lpvData=%lx\n", GetCurrentThreadId(), lpvData); 
 
   CommonFunc(); 
 
// Release the dynamic memory before the thread returns. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData != 0) 
      LocalFree((HLOCAL) lpvData); 
 
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
 
// Allocate a TLS index. 
 
   if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
      ErrorExit("TlsAlloc failed"); 
 
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
 
   for (i = 0; i < THREADCOUNT; i++) 
      WaitForSingleObject(hThread[i], INFINITE); 
 
   TlsFree(dwTlsIndex);

   return 0; 
} 
 
VOID ErrorExit (LPCSTR message)
{ 
   fprintf(stderr, "%s\n", message); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation des Stockage locaux de Thread dans une bibliothèque de Dynamic-Link](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
