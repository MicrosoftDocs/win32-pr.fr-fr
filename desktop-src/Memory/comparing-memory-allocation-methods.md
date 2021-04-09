---
Description: Voici une brève comparaison des différentes méthodes d’allocation de mémoire.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Comparaison des méthodes d’allocation de mémoire
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103953783"
---
# <a name="comparing-memory-allocation-methods"></a><span data-ttu-id="5b5ad-103">Comparaison des méthodes d’allocation de mémoire</span><span class="sxs-lookup"><span data-stu-id="5b5ad-103">Comparing Memory Allocation Methods</span></span>

<span data-ttu-id="5b5ad-104">Voici une brève comparaison des différentes méthodes d’allocation de mémoire :</span><span class="sxs-lookup"><span data-stu-id="5b5ad-104">The following is a brief comparison of the various memory allocation methods:</span></span>

-   [<span data-ttu-id="5b5ad-105">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="5b5ad-105">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [<span data-ttu-id="5b5ad-106">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="5b5ad-106">**GlobalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [<span data-ttu-id="5b5ad-107">**HeapAlloc**</span><span class="sxs-lookup"><span data-stu-id="5b5ad-107">**HeapAlloc**</span></span>](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [<span data-ttu-id="5b5ad-108">**LocalAlloc**</span><span class="sxs-lookup"><span data-stu-id="5b5ad-108">**LocalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   <span data-ttu-id="5b5ad-109">**malloc**</span><span class="sxs-lookup"><span data-stu-id="5b5ad-109">**malloc**</span></span>
-   <span data-ttu-id="5b5ad-110">**nouveau**</span><span class="sxs-lookup"><span data-stu-id="5b5ad-110">**new**</span></span>
-   [<span data-ttu-id="5b5ad-111">**VirtualAlloc**</span><span class="sxs-lookup"><span data-stu-id="5b5ad-111">**VirtualAlloc**</span></span>](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

<span data-ttu-id="5b5ad-112">Bien que les fonctions [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)et [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) allouent finalement de la mémoire à partir du même tas, chacune d’elles fournit un ensemble de fonctionnalités légèrement différent.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-112">Although the [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), and [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) functions ultimately allocate memory from the same heap, each provides a slightly different set of functionality.</span></span> <span data-ttu-id="5b5ad-113">Par exemple, **HeapAlloc** peut être invité à lever une exception si la mémoire n’a pas pu être allouée, fonctionnalité non disponible avec **LocalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-113">For example, **HeapAlloc** can be instructed to raise an exception if memory could not be allocated, a capability not available with **LocalAlloc**.</span></span> <span data-ttu-id="5b5ad-114">**LocalAlloc** prend en charge l’allocation de handles qui permettent de déplacer la mémoire sous-jacente par une réallocation sans modifier la valeur de handle, fonctionnalité non disponible avec **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-114">**LocalAlloc** supports allocation of handles which permit the underlying memory to be moved by a reallocation without changing the handle value, a capability not available with **HeapAlloc**.</span></span>

<span data-ttu-id="5b5ad-115">À partir de Windows 32 bits, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) et [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) sont implémentés en tant que fonctions wrapper qui appellent [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) à l’aide d’un handle vers le tas par défaut du processus.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-115">Starting with 32-bit Windows, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) and [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) are implemented as wrapper functions that call [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) using a handle to the process's default heap.</span></span> <span data-ttu-id="5b5ad-116">Par conséquent, **GlobalAlloc** et **LocalAlloc** ont une surcharge supérieure à **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-116">Therefore, **GlobalAlloc** and **LocalAlloc** have greater overhead than **HeapAlloc**.</span></span>

<span data-ttu-id="5b5ad-117">Étant donné que les différents allocateurs de tas fournissent des fonctionnalités distinctives à l’aide de différents mécanismes, vous devez libérer de la mémoire avec la fonction correcte.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-117">Because the different heap allocators provide distinctive functionality by using different mechanisms, you must free memory with the correct function.</span></span> <span data-ttu-id="5b5ad-118">Par exemple, la mémoire allouée avec [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) doit être libérée avec [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) et non [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) ou [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span><span class="sxs-lookup"><span data-stu-id="5b5ad-118">For example, memory allocated with [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) must be freed with [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) and not [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) or [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span></span> <span data-ttu-id="5b5ad-119">La mémoire allouée avec [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) ou [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) doit être interrogée, validée et libérée avec la fonction globale ou locale correspondante.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-119">Memory allocated with [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) or [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) must be queried, validated, and released with the corresponding global or local function.</span></span>

<span data-ttu-id="5b5ad-120">La fonction [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) vous permet de spécifier des options supplémentaires pour l’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-120">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function allows you to specify additional options for memory allocation.</span></span> <span data-ttu-id="5b5ad-121">Toutefois, ses allocations utilisent une granularité de page. par conséquent, l’utilisation de **VirtualAlloc** peut entraîner une augmentation de l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-121">However, its allocations use a page granularity, so using **VirtualAlloc** can result in higher memory usage.</span></span>

<span data-ttu-id="5b5ad-122">La fonction **malloc** présente l’inconvénient d’être dépendante de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-122">The **malloc** function has the disadvantage of being run-time dependent.</span></span> <span data-ttu-id="5b5ad-123">Le **nouvel** opérateur présente l’inconvénient de dépendre du compilateur et de la langue.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-123">The **new** operator has the disadvantage of being compiler dependent and language dependent.</span></span>

<span data-ttu-id="5b5ad-124">La fonction [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) présente l’avantage de fonctionner correctement en C, C++ ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-124">The [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function has the advantage of working well in either C, C++, or Visual Basic.</span></span> <span data-ttu-id="5b5ad-125">C’est également la seule façon de partager la mémoire dans une application COM, car MIDL utilise **CoTaskMemAlloc** et [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour marshaler la mémoire.</span><span class="sxs-lookup"><span data-stu-id="5b5ad-125">It is also the only way to share memory in a COM-based application, since MIDL uses **CoTaskMemAlloc** and [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to marshal memory.</span></span>


## <a name="examples"></a><span data-ttu-id="5b5ad-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="5b5ad-126">Examples</span></span>

* [<span data-ttu-id="5b5ad-127">Réservation et validation de la mémoire</span><span class="sxs-lookup"><span data-stu-id="5b5ad-127">Reserving and Committing Memory</span></span>](./reserving-and-committing-memory.md)

* [<span data-ttu-id="5b5ad-128">Exemple AWE</span><span class="sxs-lookup"><span data-stu-id="5b5ad-128">AWE Example</span></span>](./awe-example.md)

## <a name="related-topics"></a><span data-ttu-id="5b5ad-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b5ad-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b5ad-130">Fonctions globales et locales</span><span class="sxs-lookup"><span data-stu-id="5b5ad-130">Global and Local Functions</span></span>](global-and-local-functions.md)
</dt> <dt>

[<span data-ttu-id="5b5ad-131">Fonctions de tas</span><span class="sxs-lookup"><span data-stu-id="5b5ad-131">Heap Functions</span></span>](heap-functions.md)
</dt> <dt>

[<span data-ttu-id="5b5ad-132">Fonctions de mémoire virtuelle</span><span class="sxs-lookup"><span data-stu-id="5b5ad-132">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
</dt> </dl>

 

 