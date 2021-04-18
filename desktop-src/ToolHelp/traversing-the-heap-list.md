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
# <a name="traversing-the-heap-list"></a>Parcours de la liste des tas

L’exemple suivant obtient une liste de segments de mémoire pour le processus en cours. Il prend un instantané des tas à l’aide de la fonction [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) , puis parcourt la liste à l’aide des fonctions [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) et [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) . Pour chaque segment de mémoire, il utilise les fonctions [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) et [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) pour parcourir les blocs de tas.

> [!NOTE]
> [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) et [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) sont inefficaces, en particulier pour les grands tas. Toutefois, ils sont utiles pour interroger d’autres processus dans lesquels vous devez généralement injecter un thread dans l’autre processus pour recueillir les informations (ces API le font pour vous).

Consultez le deuxième exemple pour obtenir une alternative équivalente, bien plus efficace, qui utilise [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) au lieu de [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) et [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next). Notez que [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) peut uniquement être utilisé pour le même processus.

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

L’extrait de code suivant utilise la fonction [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) pour parcourir les tas de processus, produisant une sortie identique à l’exemple précédent, mais bien plus efficace :

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

Le parcours d’un segment de mémoire avec la fonction [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) est à peu près linéaire dans la taille du tas, tandis que le parcours d’un tas avec la fonction [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) est à peu près quadratique dans la taille du tas.
Même pour un tas modeste avec des allocations 10 000, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) s’exécute 10 000 fois plus rapidement que [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) tout en fournissant des informations plus détaillées. La différence de performance devient encore plus spectaculaire lorsque la taille du tas augmente.

Pour obtenir un exemple plus détaillé de parcours du tas avec la fonction [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) , consultez [énumération d’un segment de mémoire](/windows/win32/memory/enumerating-a-heap).
