---
title: Allocation de mémoire dans COM
description: Allocation de mémoire dans COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cb9913da55fab82f699ac05dae3998f7582224
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103887"
---
# <a name="memory-allocation-in-com"></a><span data-ttu-id="5ae8e-103">Allocation de mémoire dans COM</span><span class="sxs-lookup"><span data-stu-id="5ae8e-103">Memory Allocation in COM</span></span>

<span data-ttu-id="5ae8e-104">Parfois, une méthode alloue une mémoire tampon sur le tas et retourne l’adresse de la mémoire tampon à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-104">Sometimes a method allocates a memory buffer on the heap and returns the address of the buffer to the caller.</span></span> <span data-ttu-id="5ae8e-105">COM définit une paire de fonctions pour allouer et libérer de la mémoire sur le tas.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-105">COM defines a pair of functions for allocating and freeing memory on the heap.</span></span>

-   <span data-ttu-id="5ae8e-106">La fonction [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) alloue un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-106">The [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) function allocates a block of memory.</span></span>
-   <span data-ttu-id="5ae8e-107">La fonction [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libère un bloc de mémoire qui a été alloué avec [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span><span class="sxs-lookup"><span data-stu-id="5ae8e-107">The [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function frees a block of memory that was allocated with [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span></span>

<span data-ttu-id="5ae8e-108">Nous avons vu un exemple de ce modèle dans l' [exemple de boîte de dialogue Ouvrir](example--the-open-dialog-box.md):</span><span class="sxs-lookup"><span data-stu-id="5ae8e-108">We saw an example of this pattern in the [Open dialog box example](example--the-open-dialog-box.md):</span></span>


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



<span data-ttu-id="5ae8e-109">La méthode [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) alloue de la mémoire pour une chaîne.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-109">The [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method allocates memory for a string.</span></span> <span data-ttu-id="5ae8e-110">En interne, la méthode appelle [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-110">Internally, the method calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate the string.</span></span> <span data-ttu-id="5ae8e-111">Lorsque la méthode retourne, *pszFilePath* pointe vers l’emplacement de mémoire de la nouvelle mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-111">When the method returns, *pszFilePath* points to the memory location of the new buffer.</span></span> <span data-ttu-id="5ae8e-112">L’appelant est chargé d’appeler [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-112">The caller is responsible for calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory.</span></span>

<span data-ttu-id="5ae8e-113">Pourquoi COM définit-il ses propres fonctions d’allocation de mémoire ?</span><span class="sxs-lookup"><span data-stu-id="5ae8e-113">Why does COM define its own memory allocation functions?</span></span> <span data-ttu-id="5ae8e-114">L’une des raisons est de fournir une couche d’abstraction sur l’allocateur de tas.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-114">One reason is to provide an abstraction layer over the heap allocator.</span></span> <span data-ttu-id="5ae8e-115">Dans le cas contraire, certaines méthodes peuvent appeler **malloc** , tandis que d’autres ont appelé **New**.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-115">Otherwise, some methods might call **malloc** while others called **new**.</span></span> <span data-ttu-id="5ae8e-116">Ensuite, votre programme doit appeler **Free** dans certains cas et le **supprimer** dans d’autres, et le suivi de tout cela deviendrait rapidement impossible.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-116">Then your program would need to call **free** in some cases and **delete** in others, and keeping track of it all would quickly become impossible.</span></span> <span data-ttu-id="5ae8e-117">Les fonctions d’allocation COM créent une approche uniforme.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-117">The COM allocation functions create a uniform approach.</span></span>

<span data-ttu-id="5ae8e-118">Un autre point à prendre en compte est le fait que COM est une norme *binaire* , donc il n’est pas lié à un langage de programmation particulier.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-118">Another consideration is the fact that COM is a *binary* standard, so it is not tied to a particular programming language.</span></span> <span data-ttu-id="5ae8e-119">Par conséquent, COM ne peut pas reposer sur une forme d’allocation de mémoire propre au langage.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-119">Therefore, COM cannot rely on any language-specific form of memory allocation.</span></span>

## <a name="next"></a><span data-ttu-id="5ae8e-120">Suivant</span><span class="sxs-lookup"><span data-stu-id="5ae8e-120">Next</span></span>

[<span data-ttu-id="5ae8e-121">Pratiques de codage COM</span><span class="sxs-lookup"><span data-stu-id="5ae8e-121">COM Coding Practices</span></span>](com-coding-practices.md)

 

 
