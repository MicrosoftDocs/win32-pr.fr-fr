---
description: Allocateur de mémoire
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Allocateur de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522204"
---
# <a name="memory-allocator"></a><span data-ttu-id="b276c-103">Allocateur de mémoire</span><span class="sxs-lookup"><span data-stu-id="b276c-103">Memory Allocator</span></span>

<span data-ttu-id="b276c-104">L’objet allocateur de mémoire alloue des tampons pour les exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="b276c-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="b276c-105">Les filtres peuvent utiliser cet objet pour allouer des mémoires tampons de mémoire partagées ; Toutefois, un filtre avec des exigences spéciales peut également implémenter son propre objet allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="b276c-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="b276c-106">Créez cet objet en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b276c-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="b276c-107">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="b276c-107">Class Identifier</span></span> | <span data-ttu-id="b276c-108">CLSID \_ MemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="b276c-108">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="b276c-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="b276c-109">Interfaces</span></span>       | [<span data-ttu-id="b276c-110">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="b276c-110">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="b276c-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b276c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b276c-112">Objets DirectShow</span><span class="sxs-lookup"><span data-stu-id="b276c-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



