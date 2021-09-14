---
title: Allocateur de mémoire OLE
description: Allocateur de mémoire OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221684"
---
# <a name="the-ole-memory-allocator"></a>Allocateur de mémoire OLE

La bibliothèque COM fournit une implémentation d’un allocateur de mémoire thread-safe. (Autrement dit, il ne peut pas causer de problèmes dans les situations multithread.) Chaque fois que la propriété d’un segment de mémoire alloué est transmise via une interface COM ou entre un client et la bibliothèque COM, vous devez utiliser cet allocateur COM pour allouer la mémoire. L’allocation interne à un objet peut utiliser n’importe quel schéma d’allocation souhaité, mais l’allocateur de mémoire COM est un allocateur pratique, efficace et thread-safe.

Un appel à la fonction d’API [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) fournit un pointeur vers l’allocateur OLE, qui est une implémentation de l’interface [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) . Toutefois, il est plus efficace d’appeler les fonctions d’assistance [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)et [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), qui encapsulent un pointeur vers l’allocateur de mémoire de tâche, en appelant la méthode **IMalloc** correspondante, puis en libérant le pointeur vers l’allocateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de l’allocation de mémoire](managing-memory-allocation.md)
</dt> <dt>

[Bibliothèque COM](the-com-library.md)
</dt> </dl>

 

 