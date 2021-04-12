---
title: Débogage des allocations de mémoire
description: Débogage des allocations de mémoire
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316524"
---
# <a name="debugging-memory-allocations"></a><span data-ttu-id="9b489-103">Débogage des allocations de mémoire</span><span class="sxs-lookup"><span data-stu-id="9b489-103">Debugging Memory Allocations</span></span>

<span data-ttu-id="9b489-104">COM fournit l’interface [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) que les développeurs peuvent utiliser pour déboguer leurs allocations de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9b489-104">COM provides the [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) interface for developers to use to debug their memory allocations.</span></span> <span data-ttu-id="9b489-105">Pour chaque méthode dans [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), il existe deux méthodes dans **IMallocSpy**, une méthode « pre » et une méthode « poster ».</span><span class="sxs-lookup"><span data-stu-id="9b489-105">For each method in [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), there are two methods in **IMallocSpy**, a "pre" method and a "post" method.</span></span> <span data-ttu-id="9b489-106">Une fois qu’un développeur l’a implémenté et le publie sur le système, le système appelle la méthode « pre » **IMallocSpy** juste avant la méthode **IMalloc** correspondante, ce qui permet au code de débogage d’être « Spy » sur l’opération d’allocation et appelle la méthode « poster » pour libérer l’espion.</span><span class="sxs-lookup"><span data-stu-id="9b489-106">After a developer implements it and publishes it to the system, the system calls the **IMallocSpy** "pre" method just before the corresponding **IMalloc** method, effectively allowing the debug code to "spy" on the allocation operation, and calls the "post" method to release the spy.</span></span>

<span data-ttu-id="9b489-107">Par exemple, lorsque COM détecte que l’appel suivant est un appel à [**IMalloc :: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), il appelle [**IMallocSpy ::P realloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), en exécutant les opérations de débogage que le développeur souhaite au cours de l’exécution de l' **allocation** , puis, lorsque l’appel **alloc** est retourné, appelle [**IMallocSpy ::P ostalloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) pour libérer l’espion et retourner le contrôle au code.</span><span class="sxs-lookup"><span data-stu-id="9b489-107">For example, when COM detects that the next call is a call to [**IMalloc::Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), it calls [**IMallocSpy::PreAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), executing whatever debug operations the developer wants during the **Alloc** execution, and then, when the **Alloc** call returns, calls [**IMallocSpy::PostAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) to release the spy and return control to the code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b489-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b489-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b489-109">Gestion de l’allocation de mémoire</span><span class="sxs-lookup"><span data-stu-id="9b489-109">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> </dl>

 

 