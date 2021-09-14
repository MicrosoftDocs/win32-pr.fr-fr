---
description: Cet exemple illustre l’utilisation de la fonction GetProcessHeaps pour récupérer des handles vers le tas de processus par défaut et tous les tas privés actifs pour le processus actuel.
ms.assetid: 00f69593-f03b-4f30-aeec-db3fda0ac356
title: Obtention des tas de processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caffc8dcc69b02ab671b379dbb5e133e65f8d448
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094141"
---
# <a name="getting-process-heaps"></a>Obtention des tas de processus

Cet exemple illustre l’utilisation de la fonction [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) pour récupérer des handles vers le tas de processus par défaut et tous les tas privés actifs pour le processus actuel.

L’exemple appelle [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) deux fois, d’abord pour calculer la taille de la mémoire tampon nécessaire et à nouveau pour récupérer des handles dans la mémoire tampon. La mémoire tampon est allouée à partir du tas de processus par défaut, à l’aide du handle retourné par [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap). L’exemple imprime l’adresse de début de chaque segment de mémoire sur la console. Il utilise ensuite la fonction [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) pour libérer de la mémoire allouée pour la mémoire tampon.

Le nombre de segments dans un processus peut varier. Un processus a toujours au moins un segment de mémoire (le tas de processus par défaut) et il peut avoir un ou plusieurs tas privés créés par l’application ou par des DLL chargées dans l’espace d’adressage du processus.

Notez qu’une application doit appeler des fonctions de tas uniquement sur son tas de processus par défaut ou sur les tas privés créés par l’application ; l’appel de fonctions de tas sur un tas privé possédé par un autre composant peut entraîner un comportement indéfini.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <intsafe.h>

int __cdecl _tmain()
{
    DWORD NumberOfHeaps;
    DWORD HeapsIndex;
    DWORD HeapsLength;
    HANDLE hDefaultProcessHeap;
    HRESULT Result;
    PHANDLE aHeaps;
    SIZE_T BytesToAllocate;

    //
    // Retrieve the number of active heaps for the current process
    // so we can calculate the buffer size needed for the heap handles.
    //
    NumberOfHeaps = GetProcessHeaps(0, NULL);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve the number of heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Calculate the buffer size.
    //
    Result = SIZETMult(NumberOfHeaps, sizeof(*aHeaps), &BytesToAllocate);
    if (Result != S_OK) {
        _tprintf(TEXT("SIZETMult failed with HR %d.\n"), Result);
        return 1;
    }

    //
    // Get a handle to the default process heap.
    //
    hDefaultProcessHeap = GetProcessHeap();
    if (hDefaultProcessHeap == NULL) {
        _tprintf(TEXT("Failed to retrieve the default process heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Allocate the buffer from the default process heap.
    //
    aHeaps = (PHANDLE)HeapAlloc(hDefaultProcessHeap, 0, BytesToAllocate);
    if (aHeaps == NULL) {
        _tprintf(TEXT("HeapAlloc failed to allocate %d bytes.\n"),
                 BytesToAllocate);
        return 1;
    }

    // 
    // Save the original number of heaps because we are going to compare it
    // to the return value of the next GetProcessHeaps call.
    //
    HeapsLength = NumberOfHeaps;

    //
    // Retrieve handles to the process heaps and print them to stdout. 
    // Note that heap functions should be called only on the default heap of the process
    // or on private heaps that your component creates by calling HeapCreate.
    //
    NumberOfHeaps = GetProcessHeaps(HeapsLength, aHeaps);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }
    else if (NumberOfHeaps > HeapsLength) {

        //
        // Compare the latest number of heaps with the original number of heaps.
        // If the latest number is larger than the original number, another
        // component has created a new heap and the buffer is too small.
        //
        _tprintf(TEXT("Another component created a heap between calls. ") \
                 TEXT("Please try again.\n"));
        return 1;
    }

    _tprintf(TEXT("Process has %d heaps.\n"), HeapsLength);
    for (HeapsIndex = 0; HeapsIndex < HeapsLength; ++HeapsIndex) {
        _tprintf(TEXT("Heap %d at address: %#p.\n"),
                 HeapsIndex,
                 aHeaps[HeapsIndex]);
    }
  
    //
    // Release memory allocated from default process heap.
    //
    if (HeapFree(hDefaultProcessHeap, 0, aHeaps) == FALSE) {
        _tprintf(TEXT("Failed to free allocation from default process heap.\n"));
    }

    return 0;
}
```



 

 



