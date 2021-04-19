---
description: L’exemple suivant illustre l’utilisation des fonctions VirtualAlloc et VirtualFree pour réserver et valider la mémoire en fonction des besoins d’un tableau dynamique.
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: Réservation et validation de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ff5853d01561454265e1ee2102fbf6ebd9bb04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526990"
---
# <a name="reserving-and-committing-memory"></a><span data-ttu-id="4a084-103">Réservation et validation de la mémoire</span><span class="sxs-lookup"><span data-stu-id="4a084-103">Reserving and Committing Memory</span></span>

<span data-ttu-id="4a084-104">L’exemple suivant illustre l’utilisation des fonctions [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) et [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) pour réserver et valider la mémoire en fonction des besoins d’un tableau dynamique.</span><span class="sxs-lookup"><span data-stu-id="4a084-104">The following example illustrates the use of the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) and [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) functions in reserving and committing memory as needed for a dynamic array.</span></span> <span data-ttu-id="4a084-105">Premièrement, **VirtualAlloc** est appelé pour réserver un bloc de pages avec une **valeur null** spécifiée comme paramètre d’adresse de base, forçant le système à déterminer l’emplacement du bloc.</span><span class="sxs-lookup"><span data-stu-id="4a084-105">First, **VirtualAlloc** is called to reserve a block of pages with **NULL** specified as the base address parameter, forcing the system to determine the location of the block.</span></span> <span data-ttu-id="4a084-106">Plus tard, **VirtualAlloc** est appelé chaque fois qu’il est nécessaire de valider une page à partir de cette région réservée, et l’adresse de base de la page suivante à valider est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4a084-106">Later, **VirtualAlloc** is called whenever it is necessary to commit a page from this reserved region, and the base address of the next page to be committed is specified.</span></span>

<span data-ttu-id="4a084-107">L’exemple utilise la syntaxe de gestion structurée des exceptions pour valider les pages de la région réservée.</span><span class="sxs-lookup"><span data-stu-id="4a084-107">The example uses structured exception-handling syntax to commit pages from the reserved region.</span></span> <span data-ttu-id="4a084-108">Chaque fois qu’une exception d’erreur de page se produit pendant l’exécution du bloc **\_ \_ try** , la fonction de filtre dans l’expression qui précède le bloc **\_ \_ except** est exécutée.</span><span class="sxs-lookup"><span data-stu-id="4a084-108">Whenever a page fault exception occurs during the execution of the **\_\_try** block, the filter function in the expression preceding the **\_\_except** block is executed.</span></span> <span data-ttu-id="4a084-109">Si la fonction de filtre peut allouer une autre page, l’exécution continue dans le bloc **\_ \_ try** au point où l’exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4a084-109">If the filter function can allocate another page, execution continues in the **\_\_try** block at the point where the exception occurred.</span></span> <span data-ttu-id="4a084-110">Sinon, le gestionnaire d’exceptions dans le bloc **\_ \_ except** est exécuté.</span><span class="sxs-lookup"><span data-stu-id="4a084-110">Otherwise, the exception handler in the **\_\_except** block is executed.</span></span> <span data-ttu-id="4a084-111">Pour plus d’informations, consultez [gestion structurée des exceptions](../debug/structured-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="4a084-111">For more information, see [Structured Exception Handling](../debug/structured-exception-handling.md).</span></span>

<span data-ttu-id="4a084-112">En guise d’alternative à l’allocation dynamique, le processus peut simplement valider la région entière au lieu de la réserver uniquement.</span><span class="sxs-lookup"><span data-stu-id="4a084-112">As an alternative to dynamic allocation, the process can simply commit the entire region instead of only reserving it.</span></span> <span data-ttu-id="4a084-113">Les deux méthodes entraînent la même utilisation de la mémoire physique, car les pages validées ne consomment pas de stockage physique tant qu’elles ne sont pas accédées pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="4a084-113">Both methods result in the same physical memory usage because committed pages do not consume any physical storage until they are first accessed.</span></span> <span data-ttu-id="4a084-114">L’avantage de l’allocation dynamique est qu’elle réduit le nombre total de pages validées sur le système.</span><span class="sxs-lookup"><span data-stu-id="4a084-114">The advantage of dynamic allocation is that it minimizes the total number of committed pages on the system.</span></span> <span data-ttu-id="4a084-115">Pour les allocations très volumineuses, la prévalidation d’une allocation entière peut entraîner l’exécution du système en dehors des pages pouvant être validées, ce qui entraîne des échecs d’allocation de mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4a084-115">For very large allocations, pre-committing an entire allocation can cause the system to run out of committable pages, resulting in virtual memory allocation failures.</span></span>

<span data-ttu-id="4a084-116">La fonction [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) dans le bloc **\_ \_ except** libère automatiquement les allocations de mémoire virtuelle. il n’est donc pas nécessaire de libérer explicitement les pages lorsque le programme se termine par ce chemin d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4a084-116">The [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function in the **\_\_except** block automatically releases virtual memory allocations, so it is not necessary to explicitly free the pages when the program terminates through this execution path.</span></span> <span data-ttu-id="4a084-117">La fonction [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) libère les pages réservées et validées si le programme est généré avec la gestion des exceptions désactivée.</span><span class="sxs-lookup"><span data-stu-id="4a084-117">The [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) function frees the reserved and committed pages if the program is built with exception handling disabled.</span></span> <span data-ttu-id="4a084-118">Cette fonction utilise **la \_ libération de mem** pour annuler la validation et libérer la totalité de la région des pages réservées et validées.</span><span class="sxs-lookup"><span data-stu-id="4a084-118">This function uses **MEM\_RELEASE** to decommit and release the entire region of reserved and committed pages.</span></span>

<span data-ttu-id="4a084-119">L’exemple C++ suivant illustre l’allocation de mémoire dynamique à l’aide d’un gestionnaire d’exceptions structuré.</span><span class="sxs-lookup"><span data-stu-id="4a084-119">The following C++ example demonstrates dynamic memory allocation using a structured exception handler.</span></span>


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



 

 
