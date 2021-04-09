---
title: Allocateur de mémoire OLE
description: Allocateur de mémoire OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102397"
---
# <a name="the-ole-memory-allocator"></a><span data-ttu-id="60cd7-103">Allocateur de mémoire OLE</span><span class="sxs-lookup"><span data-stu-id="60cd7-103">The OLE Memory Allocator</span></span>

<span data-ttu-id="60cd7-104">La bibliothèque COM fournit une implémentation d’un allocateur de mémoire thread-safe.</span><span class="sxs-lookup"><span data-stu-id="60cd7-104">The COM library provides an implementation of a memory allocator that is thread-safe.</span></span> <span data-ttu-id="60cd7-105">(Autrement dit, il ne peut pas causer de problèmes dans les situations multithread.) Chaque fois que la propriété d’un segment de mémoire alloué est transmise via une interface COM ou entre un client et la bibliothèque COM, vous devez utiliser cet allocateur COM pour allouer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="60cd7-105">(That is, it cannot cause problems in multithreaded situations.) Whenever ownership of an allocated chunk of memory is passed through a COM interface or between a client and the COM library, you must use this COM allocator to allocate the memory.</span></span> <span data-ttu-id="60cd7-106">L’allocation interne à un objet peut utiliser n’importe quel schéma d’allocation souhaité, mais l’allocateur de mémoire COM est un allocateur pratique, efficace et thread-safe.</span><span class="sxs-lookup"><span data-stu-id="60cd7-106">Allocation internal to an object can use any allocation scheme desired, but the COM memory allocator is a handy, efficient, and thread-safe allocator.</span></span>

<span data-ttu-id="60cd7-107">Un appel à la fonction d’API [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) fournit un pointeur vers l’allocateur OLE, qui est une implémentation de l’interface [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) .</span><span class="sxs-lookup"><span data-stu-id="60cd7-107">A call to the API function [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) provides a pointer to the OLE allocator, which is an implementation of the [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) interface.</span></span> <span data-ttu-id="60cd7-108">Toutefois, il est plus efficace d’appeler les fonctions d’assistance [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)et [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), qui encapsulent un pointeur vers l’allocateur de mémoire de tâche, en appelant la méthode **IMalloc** correspondante, puis en libérant le pointeur vers l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="60cd7-108">However, it is more efficient to call the helper functions [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc), and [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), which wrap getting a pointer to the task memory allocator, calling the corresponding **IMalloc** method, and then releasing the pointer to the allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60cd7-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60cd7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60cd7-110">Gestion de l’allocation de mémoire</span><span class="sxs-lookup"><span data-stu-id="60cd7-110">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> <dt>

[<span data-ttu-id="60cd7-111">Bibliothèque COM</span><span class="sxs-lookup"><span data-stu-id="60cd7-111">The COM Library</span></span>](the-com-library.md)
</dt> </dl>

 

 