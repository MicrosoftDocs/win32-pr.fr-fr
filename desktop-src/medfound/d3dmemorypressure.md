---
description: Cette structure contient des données pour le rapport de sollicitation de la mémoire.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: D3DMEMORYPRESSURE, structure (D3d9types. h) pour Microsoft Media Foundation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106525696"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a><span data-ttu-id="923b6-103">D3DMEMORYPRESSURE, structure (D3d9types. h) pour Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="923b6-103">D3DMEMORYPRESSURE structure (D3d9types.h) for Microsoft Media Foundation</span></span>

<span data-ttu-id="923b6-104">Contient des données pour le signalement de la sollicitation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="923b6-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="923b6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="923b6-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="923b6-106">Membres</span><span class="sxs-lookup"><span data-stu-id="923b6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="923b6-107">**BytesEvictedFromProcess**</span><span class="sxs-lookup"><span data-stu-id="923b6-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="923b6-108">Nombre d’octets qui ont été supprimés par le processus pendant la durée de la requête.</span><span class="sxs-lookup"><span data-stu-id="923b6-108">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="923b6-109">**SizeOfInefficientAllocation**</span><span class="sxs-lookup"><span data-stu-id="923b6-109">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="923b6-110">Nombre total d’octets placés dans des segments de mémoire non optimaux, en raison d’un espace insuffisant dans les segments de mémoire préférés.</span><span class="sxs-lookup"><span data-stu-id="923b6-110">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="923b6-111">**LevelOfEfficiency**</span><span class="sxs-lookup"><span data-stu-id="923b6-111">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="923b6-112">Efficacité globale des allocations de mémoire qui ont été placées dans une mémoire non optimale.</span><span class="sxs-lookup"><span data-stu-id="923b6-112">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="923b6-113">La valeur est exprimée sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="923b6-113">The value is expressed as a percentage.</span></span> <span data-ttu-id="923b6-114">Par exemple, la valeur 95 indique que les allocations placées dans des segments de mémoire qui ne sont pas préférés sont de 95% efficaces.</span><span class="sxs-lookup"><span data-stu-id="923b6-114">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="923b6-115">Ce nombre ne doit pas être considéré comme une mesure exacte.</span><span class="sxs-lookup"><span data-stu-id="923b6-115">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="923b6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="923b6-116">Requirements</span></span>



| <span data-ttu-id="923b6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="923b6-117">Requirement</span></span> | <span data-ttu-id="923b6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="923b6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="923b6-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="923b6-119">Minimum supported client</span></span> | <span data-ttu-id="923b6-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="923b6-120">Windows 7 \[desktop apps only\]</span></span>                                                              |
| <span data-ttu-id="923b6-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="923b6-121">Minimum supported server</span></span> | <span data-ttu-id="923b6-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="923b6-122">Windows Server 2008 R2 \[desktop apps only\]</span></span>                                                 |
| <span data-ttu-id="923b6-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="923b6-123">Header</span></span>                  | <span data-ttu-id="923b6-124">D3d9types. h (inclure d3d9. h)</span><span class="sxs-lookup"><span data-stu-id="923b6-124">D3d9types.h (include D3d9.h)</span></span> |



## <a name="see-also"></a><span data-ttu-id="923b6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="923b6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="923b6-126">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="923b6-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="923b6-127">Rapport de sollicitation de la mémoire</span><span class="sxs-lookup"><span data-stu-id="923b6-127">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)
</dt> </dl>

 

 




