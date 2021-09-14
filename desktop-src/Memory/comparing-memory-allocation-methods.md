---
Description: Voici une brève comparaison des différentes méthodes d’allocation de mémoire.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Comparaison des méthodes d’allocation de mémoire
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094209"
---
# <a name="comparing-memory-allocation-methods"></a>Comparaison des méthodes d’allocation de mémoire

Voici une brève comparaison des différentes méthodes d’allocation de mémoire :

-   [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **nouveau**
-   [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

Bien que les fonctions [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)et [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) allouent finalement de la mémoire à partir du même tas, chacune d’elles fournit un ensemble de fonctionnalités légèrement différent. Par exemple, **HeapAlloc** peut être invité à lever une exception si la mémoire n’a pas pu être allouée, fonctionnalité non disponible avec **LocalAlloc**. **LocalAlloc** prend en charge l’allocation de handles qui permettent de déplacer la mémoire sous-jacente par une réallocation sans modifier la valeur de handle, fonctionnalité non disponible avec **HeapAlloc**.

à partir de 32 bits Windows, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) et [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) sont implémentés en tant que fonctions wrapper qui appellent [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) à l’aide d’un handle vers le tas par défaut du processus. Par conséquent, **GlobalAlloc** et **LocalAlloc** ont une surcharge supérieure à **HeapAlloc**.

Étant donné que les différents allocateurs de tas fournissent des fonctionnalités distinctives à l’aide de différents mécanismes, vous devez libérer de la mémoire avec la fonction correcte. Par exemple, la mémoire allouée avec [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) doit être libérée avec [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) et non [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) ou [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree). La mémoire allouée avec [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) ou [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) doit être interrogée, validée et libérée avec la fonction globale ou locale correspondante.

La fonction [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) vous permet de spécifier des options supplémentaires pour l’allocation de mémoire. Toutefois, ses allocations utilisent une granularité de page. par conséquent, l’utilisation de **VirtualAlloc** peut entraîner une augmentation de l’utilisation de la mémoire.

La fonction **malloc** présente l’inconvénient d’être dépendante de l’exécution. Le **nouvel** opérateur présente l’inconvénient de dépendre du compilateur et de la langue.

La fonction [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) présente l’avantage de fonctionner correctement en C, C++ ou Visual Basic. C’est également la seule façon de partager la mémoire dans une application COM, car MIDL utilise **CoTaskMemAlloc** et [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour marshaler la mémoire.


## <a name="examples"></a>Exemples

* [Réservation et validation de la mémoire](./reserving-and-committing-memory.md)

* [Exemple AWE](./awe-example.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions globales et locales](global-and-local-functions.md)
</dt> <dt>

[Fonctions de tas](heap-functions.md)
</dt> <dt>

[Fonctions de mémoire virtuelle](virtual-memory-functions.md)
</dt> </dl>

 

 