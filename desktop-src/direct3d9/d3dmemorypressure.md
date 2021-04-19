---
description: Contient des données pour le signalement de la sollicitation de la mémoire.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: D3DMEMORYPRESSURE, structure (D3d9types. h)
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
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527116"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a><span data-ttu-id="7a5d1-103">D3DMEMORYPRESSURE, structure (D3d9types. h)</span><span class="sxs-lookup"><span data-stu-id="7a5d1-103">D3DMEMORYPRESSURE structure (D3d9types.h)</span></span>

<span data-ttu-id="7a5d1-104">Contient des données pour le signalement de la sollicitation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="7a5d1-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5d1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a5d1-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="7a5d1-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7a5d1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a5d1-107">**BytesEvictedFromProcess**</span><span class="sxs-lookup"><span data-stu-id="7a5d1-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="7a5d1-108">Type : **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a5d1-108">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a5d1-109">Nombre d’octets qui ont été supprimés par le processus pendant la durée de la requête.</span><span class="sxs-lookup"><span data-stu-id="7a5d1-109">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="7a5d1-110">**SizeOfInefficientAllocation**</span><span class="sxs-lookup"><span data-stu-id="7a5d1-110">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="7a5d1-111">Type : **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a5d1-111">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a5d1-112">Nombre total d’octets placés dans des segments de mémoire non optimaux, en raison d’un espace insuffisant dans les segments de mémoire préférés.</span><span class="sxs-lookup"><span data-stu-id="7a5d1-112">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="7a5d1-113">**LevelOfEfficiency**</span><span class="sxs-lookup"><span data-stu-id="7a5d1-113">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="7a5d1-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a5d1-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a5d1-115">Efficacité globale des allocations de mémoire qui ont été placées dans une mémoire non optimale.</span><span class="sxs-lookup"><span data-stu-id="7a5d1-115">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="7a5d1-116">La valeur est exprimée sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="7a5d1-116">The value is expressed as a percentage.</span></span> <span data-ttu-id="7a5d1-117">Par exemple, la valeur 95 indique que les allocations placées dans des segments de mémoire qui ne sont pas préférés sont de 95% efficaces.</span><span class="sxs-lookup"><span data-stu-id="7a5d1-117">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="7a5d1-118">Ce nombre ne doit pas être considéré comme une mesure exacte.</span><span class="sxs-lookup"><span data-stu-id="7a5d1-118">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a5d1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a5d1-119">Requirements</span></span>



| <span data-ttu-id="7a5d1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a5d1-120">Requirement</span></span> | <span data-ttu-id="7a5d1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a5d1-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5d1-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a5d1-122">Header</span></span><br/> | <dl> <span data-ttu-id="7a5d1-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a5d1-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a5d1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a5d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5d1-125">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="7a5d1-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
