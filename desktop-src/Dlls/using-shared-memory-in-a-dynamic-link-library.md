---
description: L’exemple suivant montre comment la fonction de point d’entrée DLL peut utiliser un objet de mappage de fichiers pour configurer la mémoire qui peut être partagée par les processus qui chargent la DLL.
ms.assetid: ab751ab1-3b40-4111-b724-9f8676b722a3
title: Utilisation de la mémoire partagée dans une bibliothèque de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978a6fa77964c6404b3f85e9c9bcec6c3644f2ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863373"
---
# <a name="using-shared-memory-in-a-dynamic-link-library"></a>Utilisation de la mémoire partagée dans une bibliothèque de Dynamic-Link

L’exemple suivant montre comment la fonction de point d’entrée DLL peut utiliser un objet de mappage de fichiers pour configurer la mémoire qui peut être partagée par les processus qui chargent la DLL. La mémoire DLL partagée persiste uniquement tant que la DLL est chargée. Les applications peuvent utiliser les fonctions SetSharedMem et GetSharedMem pour accéder à la mémoire partagée.

## <a name="dll-that-implements-the-shared-memory"></a>DLL qui implémente la mémoire partagée

L’exemple utilise le mappage de fichiers pour mapper un bloc de mémoire partagée nommée à l’espace d’adressage virtuel de chaque processus qui charge la DLL. Pour ce faire, la fonction de point d’entrée doit :

1.  Appelez la fonction [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) pour obtenir un handle vers un objet de mappage de fichier. Le premier processus qui charge la DLL crée l’objet de mappage de fichier. Les processus suivants ouvrent un handle vers l’objet existant. Pour plus d’informations, consultez [création d’un objet File-Mapping](/windows/desktop/Memory/creating-a-file-mapping-object).
2.  Appelez la fonction [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) pour mapper une vue dans l’espace d’adressage virtuel. Cela permet au processus d’accéder à la mémoire partagée. Pour plus d’informations, consultez [création d’un affichage des fichiers](/windows/desktop/Memory/creating-a-file-view).

Notez que, bien que vous puissiez spécifier des attributs de sécurité par défaut en passant une valeur NULL pour le paramètre *lpAttributes* de [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), vous pouvez choisir d’utiliser une structure d' [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) pour renforcer la sécurité.


```C++
// The DLL code

#include <windows.h> 
#include <memory.h> 
 
#define SHMEMSIZE 4096 
 
static LPVOID lpvMem = NULL;      // pointer to shared memory
static HANDLE hMapObject = NULL;  // handle to file mapping

// The DLL entry-point function sets up shared memory using a 
// named file-mapping object. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL,  // DLL module handle
    DWORD fdwReason,              // reason called 
    LPVOID lpvReserved)           // reserved 
{ 
    BOOL fInit, fIgnore; 
 
    switch (fdwReason) 
    { 
        // DLL load due to process initialization or LoadLibrary
 
          case DLL_PROCESS_ATTACH: 
 
            // Create a named file mapping object
 
            hMapObject = CreateFileMapping( 
                INVALID_HANDLE_VALUE,   // use paging file
                NULL,                   // default security attributes
                PAGE_READWRITE,         // read/write access
                0,                      // size: high 32-bits
                SHMEMSIZE,              // size: low 32-bits
                TEXT("dllmemfilemap")); // name of map object
            if (hMapObject == NULL) 
                return FALSE; 
 
            // The first process to attach initializes memory
 
            fInit = (GetLastError() != ERROR_ALREADY_EXISTS); 
 
            // Get a pointer to the file-mapped shared memory
 
            lpvMem = MapViewOfFile( 
                hMapObject,     // object to map view of
                FILE_MAP_WRITE, // read/write access
                0,              // high offset:  map from
                0,              // low offset:   beginning
                0);             // default: map entire file
            if (lpvMem == NULL) 
                return FALSE; 
 
            // Initialize memory if this is the first process
 
            if (fInit) 
                memset(lpvMem, '\0', SHMEMSIZE); 
 
            break; 
 
        // The attached process creates a new thread
 
        case DLL_THREAD_ATTACH: 
            break; 
 
        // The thread of the attached process terminates
 
        case DLL_THREAD_DETACH: 
            break; 
 
        // DLL unload due to process termination or FreeLibrary
 
        case DLL_PROCESS_DETACH: 
 
            // Unmap shared memory from the process's address space
 
            fIgnore = UnmapViewOfFile(lpvMem); 
 
            // Close the process's handle to the file-mapping object
 
            fIgnore = CloseHandle(hMapObject); 
 
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
 
// SetSharedMem sets the contents of the shared memory 
 
__declspec(dllexport) VOID __cdecl SetSharedMem(LPWSTR lpszBuf) 
{ 
    LPWSTR lpszTmp; 
    DWORD dwCount=1;
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy the null-terminated string into shared memory
 
    while (*lpszBuf && dwCount<SHMEMSIZE) 
    {
        *lpszTmp++ = *lpszBuf++; 
        dwCount++;
    }
    *lpszTmp = '\0'; 
} 
 
// GetSharedMem gets the contents of the shared memory
 
__declspec(dllexport) VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize) 
{ 
    LPWSTR lpszTmp; 
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy from shared memory into the caller's buffer
 
    while (*lpszTmp && --cchSize) 
        *lpszBuf++ = *lpszTmp++; 
    *lpszBuf = '\0'; 
}
#ifdef __cplusplus
}
#endif
```



La mémoire partagée peut être mappée à une adresse différente dans chaque processus. Pour cette raison, chaque processus possède sa propre instance de lpvMem, qui est déclarée en tant que variable globale afin d’être disponible pour toutes les fonctions DLL. L’exemple suppose que les données globales de la DLL ne sont pas partagées, donc chaque processus qui charge la DLL possède sa propre instance de lpvMem.

Notez que la mémoire partagée est libérée lorsque le dernier descripteur de l’objet de mappage de fichier est fermé. Pour créer une mémoire partagée persistante, vous devez vous assurer qu’un processus a toujours un handle ouvert pour l’objet de mappage de fichier.

## <a name="processes-that-use-the-shared-memory"></a>Processus qui utilisent la mémoire partagée

Les processus suivants utilisent la mémoire partagée fournie par la DLL définie ci-dessus. Le premier processus appelle SetSharedMem pour écrire une chaîne tandis que le deuxième processus appelle GetSharedMem pour récupérer cette chaîne.

Ce processus utilise la fonction SetSharedMem implémentée par la DLL pour écrire la chaîne « This is a test string » dans la mémoire partagée. Il démarre également un processus enfant qui lira la chaîne à partir de la mémoire partagée.


```C++
// Parent process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl SetSharedMem(LPWSTR lpszBuf);

HANDLE CreateChildProcess(LPTSTR szCmdline) 
{ 
   PROCESS_INFORMATION piProcInfo; 
   STARTUPINFO siStartInfo;
   BOOL bFuncRetn = FALSE; 
 
// Set up members of the PROCESS_INFORMATION structure. 
 
   ZeroMemory( &piProcInfo, sizeof(PROCESS_INFORMATION) );
 
// Set up members of the STARTUPINFO structure. 
 
   ZeroMemory( &siStartInfo, sizeof(STARTUPINFO) );
   siStartInfo.cb = sizeof(STARTUPINFO); 
 
// Create the child process. 
    
   bFuncRetn = CreateProcess(NULL, 
      szCmdline,     // command line 
      NULL,          // process security attributes 
      NULL,          // primary thread security attributes 
      TRUE,          // handles are inherited 
      0,             // creation flags 
      NULL,          // use parent's environment 
      NULL,          // use parent's current directory 
      &siStartInfo,  // STARTUPINFO pointer 
      &piProcInfo);  // receives PROCESS_INFORMATION 
   
   if (bFuncRetn == 0) 
   {
      printf("CreateProcess failed (%)\n", GetLastError());
      return INVALID_HANDLE_VALUE;
   }
   else 
   {
      CloseHandle(piProcInfo.hThread);
      return piProcInfo.hProcess;
   }
}

int _tmain(int argc, TCHAR *argv[])
{
   HANDLE hProcess;

   if (argc == 1) 
   {
      printf("Please specify an input file");
      ExitProcess(0);
   }

   // Call the DLL function
   printf("\nProcess is writing to shared memory...\n\n");
   SetSharedMem(L"This is a test string");

   // Start the child process that will read the memory
   hProcess = CreateChildProcess(argv[1]);

   // Ensure this process is around until the child process terminates
   if (INVALID_HANDLE_VALUE != hProcess) 
   {
      WaitForSingleObject(hProcess, INFINITE);
      CloseHandle(hProcess);
   }
   return 0;
}

```



Ce processus utilise la fonction GetSharedMem implémentée par la DLL pour lire une chaîne à partir de la mémoire partagée. Elle est démarrée par le processus parent ci-dessus.


```C++
// Child process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize);

int _tmain( void )
{
    WCHAR cBuf[MAX_PATH];

    GetSharedMem(cBuf, MAX_PATH);
 
    printf("Child process read from shared memory: %S\n", cBuf);
    
    return 0;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Données de bibliothèque de liens dynamiques](dynamic-link-library-data.md)
</dt> </dl>

 

 
