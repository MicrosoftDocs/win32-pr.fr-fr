---
title: Sous-allocation au sein des tas
description: Les tas de ressources transfèrent les données de l’UC vers le GPU (chargement) et du GPU vers le processeur (lecture en retour).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104619"
---
# <a name="suballocation-within-heaps"></a><span data-ttu-id="4c176-103">Sous-allocation au sein des tas</span><span class="sxs-lookup"><span data-stu-id="4c176-103">Suballocation Within Heaps</span></span>

<span data-ttu-id="4c176-104">Les tas de ressources transfèrent les données de l’UC vers le GPU (chargement) et du GPU vers le processeur (lecture en retour).</span><span class="sxs-lookup"><span data-stu-id="4c176-104">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4c176-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="4c176-105">In this section</span></span>



| <span data-ttu-id="4c176-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="4c176-106">Topic</span></span>                                                                                       | <span data-ttu-id="4c176-107">Description</span><span class="sxs-lookup"><span data-stu-id="4c176-107">Description</span></span>                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c176-108">Alias de mémoire et héritage de données</span><span class="sxs-lookup"><span data-stu-id="4c176-108">Memory Aliasing and Data Inheritance</span></span>](memory-aliasing-and-data-inheritance.md)<br/> | <span data-ttu-id="4c176-109">Les ressources placées et réservées peuvent avoir un alias de la mémoire physique dans un segment.</span><span class="sxs-lookup"><span data-stu-id="4c176-109">Placed and reserved resource may alias physical memory within a heap.</span></span> <span data-ttu-id="4c176-110">Les ressources passées activent davantage de scénarios d’héritage de données que les ressources réservées lorsque l’indicateur partagé est défini pour le tas ou lorsque les ressources avec alias ont des dispositions de mémoire entièrement définies.</span><span class="sxs-lookup"><span data-stu-id="4c176-110">Placed resources enable more data inheritance scenarios than reserved resources when the heap has the shared flag set or when the aliased resources have fully defined memory layouts.</span></span> <br/> |
| [<span data-ttu-id="4c176-111">Tas partagés</span><span class="sxs-lookup"><span data-stu-id="4c176-111">Shared Heaps</span></span>](shared-heaps.md)<br/>                                                 | <span data-ttu-id="4c176-112">Le partage est utile pour les architectures multiprocessus et multi-adaptateurs.</span><span class="sxs-lookup"><span data-stu-id="4c176-112">Sharing is useful for multi-process and multi-adapter architectures.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="4c176-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c176-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c176-114">**ID3D12Device :: CreateHeap**</span><span class="sxs-lookup"><span data-stu-id="4c176-114">**ID3D12Device::CreateHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[<span data-ttu-id="4c176-115">**ID3D12Heap**</span><span class="sxs-lookup"><span data-stu-id="4c176-115">**ID3D12Heap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[<span data-ttu-id="4c176-116">Gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="4c176-116">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





