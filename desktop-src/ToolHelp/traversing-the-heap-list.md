---
title: Parcours de la liste des tas
description: Exemples montrant comment obtenir une liste de segments de mémoire pour le processus actuel.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 5cc555f9a94166fa181309985d8a49c686baf06c
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "106533288"
---
# <a name="traversing-the-heap-list"></a><span data-ttu-id="e030f-103">Parcours de la liste des tas</span><span class="sxs-lookup"><span data-stu-id="e030f-103">Traversing the Heap List</span></span>

<span data-ttu-id="e030f-104">L’exemple suivant obtient une liste de segments de mémoire pour le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="e030f-104">The following example obtains a list of heaps for the current process.</span></span> <span data-ttu-id="e030f-105">Il prend un instantané des tas à l’aide de la fonction [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) , puis parcourt la liste à l’aide des fonctions [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) et [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) .</span><span class="sxs-lookup"><span data-stu-id="e030f-105">It takes a snapshot of the heaps using the [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) function, and then walks through the list using the [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) and [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) functions.</span></span> <span data-ttu-id="e030f-106">Pour chaque segment de mémoire, il utilise les fonctions [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) et [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) pour parcourir les blocs de tas.</span><span class="sxs-lookup"><span data-stu-id="e030f-106">For each heap, it uses the [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) functions to walk the heap blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="e030f-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) et [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) sont inefficaces, en particulier pour les grands tas.</span><span class="sxs-lookup"><span data-stu-id="e030f-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) are inefficient, particularly for large heaps.</span></span> <span data-ttu-id="e030f-108">Toutefois, ils sont utiles pour interroger d’autres processus dans lesquels vous devez généralement injecter un thread dans l’autre processus pour recueillir les informations (ces API le font pour vous).</span><span class="sxs-lookup"><span data-stu-id="e030f-108">However, they are useful for querying other processes where you'd typically have to inject a thread into the other process to gather the information (these APIs do this for you).</span></span>

<span data-ttu-id="e030f-109">Consultez le deuxième exemple pour obtenir une alternative équivalente, bien plus efficace, qui utilise [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) au lieu de [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) et [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span><span class="sxs-lookup"><span data-stu-id="e030f-109">See the second example for an equivalent, much more efficient, alternative that uses [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) instead of [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span></span> <span data-ttu-id="e030f-110">Notez que [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) peut uniquement être utilisé pour le même processus.</span><span class="sxs-lookup"><span data-stu-id="e030f-110">Note that [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) can only be used for the same process.</span></span>

```C++
#include <windows.h>
#include <tlhelp32.h>
#include <stdio.h>

int main( void )
{
   HEAPLIST32 hl;
   
   HANDLE hHeapSnap = CreateToolhelp32Snapshot(TH32CS_SNAPHEAPLIST, GetCurrentProcessId());
   
   hl.dwSize = sizeof(HEAPLIST32);
   
   if ( hHeapSnap == INVALID_HANDLE_VALUE )
   {
      printf ("CreateToolhelp32Snapshot failed (%d)\n", GetLastError());
      return 1;
   }
   
   if( Heap32ListFirst( hHeapSnap, &hl ) )
   {
      do
      {
         HEAPENTRY32 he;
         ZeroMemory(&he, sizeof(HEAPENTRY32));
         he.dwSize = sizeof(HEAPENTRY32);

         if( Heap32First( &he, GetCurrentProcessId(), hl.th32HeapID ) )
         {
            printf( "\nHeap ID: %d\n", hl.th32HeapID );
            do
            {
               printf( "Block size: %d\n", he.dwBlockSize );
               
               he.dwSize = sizeof(HEAPENTRY32);
            } while( Heap32Next(&he) );
         }
         hl.dwSize = sizeof(HEAPLIST32);
      } while (Heap32ListNext( hHeapSnap, &hl ));
   }
   else printf ("Cannot list first heap (%d)\n", GetLastError());
   
   CloseHandle(hHeapSnap); 

   return 0;
}
```

<span data-ttu-id="e030f-111">L’extrait de code suivant utilise la fonction [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) pour parcourir les tas de processus, produisant une sortie identique à l’exemple précédent, mais bien plus efficace :</span><span class="sxs-lookup"><span data-stu-id="e030f-111">The following code snippet uses the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function to walk the process heaps, producing identical output to the previous example, but much more efficiently:</span></span>

```C++
#include <windows.h>
#include <stdio.h>

int main( void )
{
    DWORD heapIndex;
    DWORD heapCount = 0;
    PHANDLE heaps = NULL;
    while (TRUE)
    {
        DWORD actualHeapCount = GetProcessHeaps(heapCount, heaps);
        if (actualHeapCount <= heapCount)
        {
            break;
        }
        heapCount = actualHeapCount;
        free(heaps);
        heaps = (HANDLE*)malloc(heapCount * sizeof(HANDLE));
        if (heaps == NULL)
        {
            printf("Unable to allocate memory for list of heaps\n");
            return 1;
        }
    }

    for (heapIndex = 0; heapIndex < heapCount; heapIndex++)
    {
        PROCESS_HEAP_ENTRY entry;

        printf("Heap ID: %d\n", (DWORD)(ULONG_PTR)heaps[heapIndex]);
        entry.lpData = NULL;
        while (HeapWalk(heaps[heapIndex], &entry))
        {
            // Heap32First and Heap32Next ignore entries
            // with the PROCESS_HEAP_REGION flag
            if (!(entry.wFlags & PROCESS_HEAP_REGION))
            {
                printf("Block size: %d\n", entry.cbData + entry.cbOverhead);
            }
        }
    }

    free(heaps);
    return 0;
}
```

<span data-ttu-id="e030f-112">Le parcours d’un segment de mémoire avec la fonction [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) est à peu près linéaire dans la taille du tas, tandis que le parcours d’un tas avec la fonction [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) est à peu près quadratique dans la taille du tas.</span><span class="sxs-lookup"><span data-stu-id="e030f-112">Walking a heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function is roughly linear in the size of the heap, whereas walking a heap with the [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) function is roughly quadratic in the size of the heap.</span></span>
<span data-ttu-id="e030f-113">Même pour un tas modeste avec des allocations 10 000, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) s’exécute 10 000 fois plus rapidement que [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) tout en fournissant des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="e030f-113">Even for a modest heap with 10,000 allocations, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) runs 10,000 times faster than [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) while providing more detailed information.</span></span> <span data-ttu-id="e030f-114">La différence de performance devient encore plus spectaculaire lorsque la taille du tas augmente.</span><span class="sxs-lookup"><span data-stu-id="e030f-114">The difference in performance becomes even more dramatic as the heap size increases.</span></span>

<span data-ttu-id="e030f-115">Pour obtenir un exemple plus détaillé de parcours du tas avec la fonction [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) , consultez [énumération d’un segment de mémoire](/windows/win32/memory/enumerating-a-heap).</span><span class="sxs-lookup"><span data-stu-id="e030f-115">For a more detailed example of walking the heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function, see [Enumerating a Heap](/windows/win32/memory/enumerating-a-heap).</span></span>
