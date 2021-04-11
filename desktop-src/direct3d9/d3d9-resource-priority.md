---
description: Constantes utilisées pour définir la priorité d’une ressource dans SetPriority.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211713"
---
# <a name="d3d9_resource_priority"></a><span data-ttu-id="cf8a5-103">Priorité de la \_ ressource d3d9 \_</span><span class="sxs-lookup"><span data-stu-id="cf8a5-103">D3D9\_RESOURCE\_PRIORITY</span></span>

<span data-ttu-id="cf8a5-104">Constantes utilisées pour définir la priorité d’une ressource dans [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span><span class="sxs-lookup"><span data-stu-id="cf8a5-104">Constants used to set the priority of a resource in [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span></span>



| <span data-ttu-id="cf8a5-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="cf8a5-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="cf8a5-106">Description</span><span class="sxs-lookup"><span data-stu-id="cf8a5-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <span data-ttu-id="cf8a5-107"><dt>**D3d9 \_ 0x28000000 \_ \_ minimale**</dt> de la priorité de ressource <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cf8a5-107"><dt>**D3D9\_RESOURCE\_PRIORITY\_MINIMUM**</dt> <dt>0x28000000</dt></span></span> </dl> | <span data-ttu-id="cf8a5-108">La ressource a la priorité la plus faible possible.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-108">The resource has the lowest priority possible.</span></span> <span data-ttu-id="cf8a5-109">Cette constante marque la ressource comme inutilisée et pour l’éviction.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-109">This constant marks the resource as unused and for eviction.</span></span> <span data-ttu-id="cf8a5-110">La ressource doit être supprimée dès qu’une autre ressource requiert l’espace mémoire occupé par la ressource.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-110">The resource should be evicted as soon as another resource requires the memory space that the resource occupies.</span></span><br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <span data-ttu-id="cf8a5-111"><dt>**D3d9 \_ Priorité de ressource \_ \_ basse**</dt> <dt>0x50000000</dt></span><span class="sxs-lookup"><span data-stu-id="cf8a5-111"><dt>**D3D9\_RESOURCE\_PRIORITY\_LOW**</dt> <dt>0x50000000</dt></span></span> </dl>             | <span data-ttu-id="cf8a5-112">La ressource est planifiée avec une priorité basse.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-112">The resource is scheduled with low priority.</span></span> <span data-ttu-id="cf8a5-113">Le placement de la ressource n’est pas critique et le système d’exploitation effectue un travail minimal pour rechercher un emplacement pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-113">The placement of the resource is not critical, and the operating system performs minimal work to find a location for the resource.</span></span> <span data-ttu-id="cf8a5-114">Le marquage d’une ressource en basse priorité permet d’autres ressources plus critiques d’occuper la mémoire la plus rapide.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-114">Marking a resource as low priority allows other more critical resources to occupy the faster memory.</span></span><br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <span data-ttu-id="cf8a5-115"><dt>**D3d9 \_ 0x78000000 \_ \_ normale de priorité de ressource**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cf8a5-115"><dt>**D3D9\_RESOURCE\_PRIORITY\_NORMAL**</dt> <dt>0x78000000</dt></span></span> </dl>    | <span data-ttu-id="cf8a5-116">La ressource est planifiée avec une priorité normale.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-116">The resource is scheduled with normal priority.</span></span> <span data-ttu-id="cf8a5-117">La position de la ressource est importante pour les performances, mais elle n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-117">The placement of the resource is important for performance, but it is not critical.</span></span> <span data-ttu-id="cf8a5-118">Le système d’exploitation doit tenter de placer la ressource qui est marquée comme normale à l’emplacement préféré de la ressource au lieu d’une ressource de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-118">The operating system should try to place the resource that is marked as normal in the resource's preferred location instead of a low-priority resource.</span></span> <span data-ttu-id="cf8a5-119">En règle générale, les textures sont marquées comme normales.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-119">Typically, textures are marked as normal.</span></span><br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <span data-ttu-id="cf8a5-120"><dt>**D3d9 \_ Priorité de ressource \_ \_ élevée**</dt> <dt>0xA0000000</dt></span><span class="sxs-lookup"><span data-stu-id="cf8a5-120"><dt>**D3D9\_RESOURCE\_PRIORITY\_HIGH**</dt> <dt>0xa0000000</dt></span></span> </dl>          | <span data-ttu-id="cf8a5-121">La ressource est planifiée avec une priorité élevée.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-121">The resource is scheduled with high priority.</span></span> <span data-ttu-id="cf8a5-122">Le positionnement de la ressource est essentiel pour les performances.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-122">The placement of the resource is critical for performance.</span></span> <span data-ttu-id="cf8a5-123">Le système d’exploitation tente toujours de placer la ressource marquée comme haute dans l’emplacement préféré de la ressource au lieu d’une ressource de priorité basse ou normale.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-123">The operating system always tries to place the resource that is marked as high in the resource's preferred location instead of a low-priority or normal-priority resource.</span></span> <span data-ttu-id="cf8a5-124">En général, les cibles de rendu sont marquées comme étant élevées.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-124">Typically, render targets are marked as high.</span></span><br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <span data-ttu-id="cf8a5-125"><dt>**D3d9 \_ 0xc8000000 \_ \_ maximale**</dt> de la priorité de ressource <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cf8a5-125"><dt>**D3D9\_RESOURCE\_PRIORITY\_MAXIMUM**</dt> <dt>0xc8000000</dt></span></span> </dl> | <span data-ttu-id="cf8a5-126">La ressource a la priorité maximale possible.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-126">The resource has the maximum priority possible.</span></span> <span data-ttu-id="cf8a5-127">Cette constante marque la priorité de la ressource comme étant épinglée de manière réversible.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-127">This constant marks the priority of the resource as soft-pinned.</span></span> <span data-ttu-id="cf8a5-128">Une ressource épinglée n’est supprimée de la mémoire que s’il n’existe aucune autre façon de résoudre la mémoire requise d’une mémoire tampon DMA.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-128">A soft-pinned resource is evicted from memory only if there is no other way of resolving the memory requirement of a DMA buffer.</span></span> <span data-ttu-id="cf8a5-129">Le système d’exploitation tente de fractionner une mémoire tampon DMA à sa taille minimale et supprime toutes les autres ressources qui ne sont pas épinglées et qui ne sont pas épinglées de manière réversible avant de supprimer une ressource épinglée.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-129">The operating system attempts to split a DMA buffer to its minimum size and evict all other resources that are not pinned and not soft-pinned before it evicts a soft-pinned resource.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="cf8a5-130">Notes</span><span class="sxs-lookup"><span data-stu-id="cf8a5-130">Remarks</span></span>

<span data-ttu-id="cf8a5-131">Les valeurs autres que la priorité de **\_ ressource d3d9 \_ \_ minimale** et la **priorité de \_ ressource d3d9 \_ \_ maximale** sont traitées comme des indicateurs par le planificateur.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-131">Values other than **D3D9\_RESOURCE\_PRIORITY\_MINIMUM** and **D3D9\_RESOURCE\_PRIORITY\_MAXIMUM** are treated as hints by the scheduler.</span></span>

<span data-ttu-id="cf8a5-132">Vous pouvez utiliser des niveaux de priorité autres que les valeurs définies précédemment dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-132">You can use priority levels other than the values defined earlier in this topic.</span></span> <span data-ttu-id="cf8a5-133">Par exemple, le marquage d’une ressource avec un niveau de priorité de 0x78000001 indique que la priorité de la ressource est légèrement supérieure à la normale.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-133">For example, marking a resource with a priority level of 0x78000001 indicates that the resource priority is slightly above normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8a5-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf8a5-134">Requirements</span></span>



| <span data-ttu-id="cf8a5-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf8a5-135">Requirement</span></span> | <span data-ttu-id="cf8a5-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf8a5-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8a5-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf8a5-137">Header</span></span><br/> | <dl> <span data-ttu-id="cf8a5-138"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf8a5-138"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf8a5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf8a5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8a5-140">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="cf8a5-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
