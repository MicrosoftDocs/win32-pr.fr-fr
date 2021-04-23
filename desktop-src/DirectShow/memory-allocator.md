---
description: Allocateur de mémoire
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Allocateur de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909418"
---
# <a name="memory-allocator"></a><span data-ttu-id="1895f-103">Allocateur de mémoire</span><span class="sxs-lookup"><span data-stu-id="1895f-103">Memory Allocator</span></span>

<span data-ttu-id="1895f-104">L’objet allocateur de mémoire alloue des tampons pour les exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="1895f-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="1895f-105">Les filtres peuvent utiliser cet objet pour allouer des mémoires tampons de mémoire partagées ; Toutefois, un filtre avec des exigences spéciales peut également implémenter son propre objet allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1895f-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="1895f-106">Créez cet objet en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="1895f-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="1895f-107">Étiquette</span><span class="sxs-lookup"><span data-stu-id="1895f-107">Label</span></span> | <span data-ttu-id="1895f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="1895f-108">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="1895f-109">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="1895f-109">Class Identifier</span></span> | <span data-ttu-id="1895f-110">CLSID \_ MemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="1895f-110">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="1895f-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="1895f-111">Interfaces</span></span>       | [<span data-ttu-id="1895f-112">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="1895f-112">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="1895f-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1895f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1895f-114">Objets DirectShow</span><span class="sxs-lookup"><span data-stu-id="1895f-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



