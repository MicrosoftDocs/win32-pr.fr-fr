---
description: L’exemple suivant illustre l’utilisation des fonctions VirtualAlloc et VirtualFree pour réserver et valider la mémoire en fonction des besoins d’un tableau dynamique.
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: Réservation et validation de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615f3c4321dc432b5ef83a841cea12215563e7d103443512a4d3b2c553849540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386277"
---
# <a name="reserving-and-committing-memory"></a>Réservation et validation de la mémoire

L’exemple suivant illustre l’utilisation des fonctions [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) et [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) pour réserver et valider la mémoire en fonction des besoins d’un tableau dynamique. Premièrement, **VirtualAlloc** est appelé pour réserver un bloc de pages avec une **valeur null** spécifiée comme paramètre d’adresse de base, forçant le système à déterminer l’emplacement du bloc. Plus tard, **VirtualAlloc** est appelé chaque fois qu’il est nécessaire de valider une page à partir de cette région réservée, et l’adresse de base de la page suivante à valider est spécifiée.

L’exemple utilise la syntaxe de gestion structurée des exceptions pour valider les pages de la région réservée. Chaque fois qu’une exception d’erreur de page se produit pendant l’exécution du bloc **\_ \_ try** , la fonction de filtre dans l’expression qui précède le bloc **\_ \_ except** est exécutée. Si la fonction de filtre peut allouer une autre page, l’exécution continue dans le bloc **\_ \_ try** au point où l’exception s’est produite. Sinon, le gestionnaire d’exceptions dans le bloc **\_ \_ except** est exécuté. Pour plus d’informations, consultez [gestion structurée des exceptions](../debug/structured-exception-handling.md).

En guise d’alternative à l’allocation dynamique, le processus peut simplement valider la région entière au lieu de la réserver uniquement. Les deux méthodes entraînent la même utilisation de la mémoire physique, car les pages validées ne consomment pas de stockage physique tant qu’elles ne sont pas accédées pour la première fois. L’avantage de l’allocation dynamique est qu’elle réduit le nombre total de pages validées sur le système. Pour les allocations très volumineuses, la prévalidation d’une allocation entière peut entraîner l’exécution du système en dehors des pages pouvant être validées, ce qui entraîne des échecs d’allocation de mémoire virtuelle.

La fonction [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) dans le bloc **\_ \_ except** libère automatiquement les allocations de mémoire virtuelle. il n’est donc pas nécessaire de libérer explicitement les pages lorsque le programme se termine par ce chemin d’exécution. La fonction [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) libère les pages réservées et validées si le programme est généré avec la gestion des exceptions désactivée. Cette fonction utilise **la \_ libération de mem** pour annuler la validation et libérer la totalité de la région des pages réservées et validées.

L’exemple C++ suivant illustre l’allocation de mémoire dynamique à l’aide d’un gestionnaire d’exceptions structuré.


```C++
// A short program to demonstrate dynamic memory allocation
// using a structured exception handler.

#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <stdlib.h>             // For exit

#define PAGELIMIT 80            // Number of pages to ask for

LPTSTR lpNxtPage;               // Address of the next page to ask for
DWORD dwPages = 0;              // Count of pages gotten so far
DWORD dwPageSize;               // Page size on this computer

INT PageFaultExceptionFilter(DWORD dwCode)
{
    LPVOID lpvResult;

    // If the exception is not a page fault, exit.

    if (dwCode != EXCEPTION_ACCESS_VIOLATION)
    {
        _tprintf(TEXT("Exception code = %d.\n"), dwCode);
        return EXCEPTION_EXECUTE_HANDLER;
    }

    _tprintf(TEXT("Exception is a page fault.\n"));

    // If the reserved pages are used up, exit.

    if (dwPages >= PAGELIMIT)
    {
        _tprintf(TEXT("Exception: out of pages.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }

    // Otherwise, commit another page.

    lpvResult = VirtualAlloc(
                     (LPVOID) lpNxtPage, // Next page to commit
                     dwPageSize,         // Page size, in bytes
                     MEM_COMMIT,         // Allocate a committed page
                     PAGE_READWRITE);    // Read/write access
    if (lpvResult == NULL )
    {
        _tprintf(TEXT("VirtualAlloc failed.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }
    else
    {
        _tprintf(TEXT("Allocating another page.\n"));
    }

    // Increment the page count, and advance lpNxtPage to the next page.

    dwPages++;
    lpNxtPage = (LPTSTR) ((PCHAR) lpNxtPage + dwPageSize);

    // Continue execution where the page fault occurred.

    return EXCEPTION_CONTINUE_EXECUTION;
}

VOID ErrorExit(LPTSTR lpMsg)
{
    _tprintf(TEXT("Error! %s with error code of %ld.\n"),
             lpMsg, GetLastError ());
    exit (0);
}

VOID _tmain(VOID)
{
    LPVOID lpvBase;               // Base address of the test memory
    LPTSTR lpPtr;                 // Generic character pointer
    BOOL bSuccess;                // Flag
    DWORD i;                      // Generic counter
    SYSTEM_INFO sSysInfo;         // Useful information about the system

    GetSystemInfo(&sSysInfo);     // Initialize the structure.

    _tprintf (TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

    dwPageSize = sSysInfo.dwPageSize;

    // Reserve pages in the virtual address space of the process.

    lpvBase = VirtualAlloc(
                     NULL,                 // System selects address
                     PAGELIMIT*dwPageSize, // Size of allocation
                     MEM_RESERVE,          // Allocate reserved pages
                     PAGE_NOACCESS);       // Protection = no access
    if (lpvBase == NULL )
        ErrorExit(TEXT("VirtualAlloc reserve failed."));

    lpPtr = lpNxtPage = (LPTSTR) lpvBase;

    // Use structured exception handling when accessing the pages.
    // If a page fault occurs, the exception filter is executed to
    // commit another page from the reserved block of pages.

    for (i=0; i < PAGELIMIT*dwPageSize; i++)
    {
        __try
        {
            // Write to memory.

            lpPtr[i] = 'a';
        }

        // If there's a page fault, commit another page and try again.

        __except ( PageFaultExceptionFilter( GetExceptionCode() ) )
        {

            // This code is executed only if the filter function
            // is unsuccessful in committing the next page.

            _tprintf (TEXT("Exiting process.\n"));

            ExitProcess( GetLastError() );

        }

    }

    // Release the block of pages when you are finished using them.

    bSuccess = VirtualFree(
                       lpvBase,       // Base address of block
                       0,             // Bytes of committed pages
                       MEM_RELEASE);  // Decommit the pages

    _tprintf (TEXT("Release %s.\n"), bSuccess ? TEXT("succeeded") : TEXT("failed") );

}
```



 

 
