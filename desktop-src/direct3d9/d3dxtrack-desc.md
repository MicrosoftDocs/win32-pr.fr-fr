---
description: Décrit une piste d’animation et spécifie le poids de fusion, la vitesse et la position de la piste à un moment donné.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: Structure D3DXTRACK_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542155"
---
# <a name="d3dxtrack_desc-structure"></a><span data-ttu-id="ad5c7-103">D3DXTRACK \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="ad5c7-103">D3DXTRACK\_DESC structure</span></span>

<span data-ttu-id="ad5c7-104">Décrit une piste d’animation et spécifie le poids de fusion, la vitesse et la position de la piste à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-104">Describes an animation track and specifies blending weight, speed, and position for the track at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad5c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad5c7-105">Syntax</span></span>


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a><span data-ttu-id="ad5c7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ad5c7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ad5c7-107">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="ad5c7-107">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="ad5c7-108">Type : **[ **D3DXPRIORITY \_**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ad5c7-108">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad5c7-109">Type de priorité, tel que défini dans [**D3DXPRIORITY \_ type**](./d3dxpriority-type.md).</span><span class="sxs-lookup"><span data-stu-id="ad5c7-109">Priority type, as defined in [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad5c7-110">**Poids**</span><span class="sxs-lookup"><span data-stu-id="ad5c7-110">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="ad5c7-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad5c7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad5c7-112">Valeur de poids.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-112">Weight value.</span></span> <span data-ttu-id="ad5c7-113">Le poids détermine la proportion de cette piste à mélanger avec d’autres pistes.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-113">The weight determines the proportion of this track to blend with other tracks.</span></span>

</dd> <dt>

<span data-ttu-id="ad5c7-114">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="ad5c7-114">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="ad5c7-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad5c7-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad5c7-116">Valeur de vitesse.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-116">Speed value.</span></span> <span data-ttu-id="ad5c7-117">Cela est utilisé de la même façon qu’un multiplicateur pour mettre à l’échelle la période de la piste.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-117">This is used similarly to a multiplier to scale the period of the track.</span></span>

</dd> <dt>

<span data-ttu-id="ad5c7-118">**Position**</span><span class="sxs-lookup"><span data-stu-id="ad5c7-118">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="ad5c7-119">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad5c7-119">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad5c7-120">Position horaire de la piste, dans la plage locale de son ensemble d’animations actuel.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-120">Time position of the track, in the local timeframe of its current animation set.</span></span>

</dd> <dt>

<span data-ttu-id="ad5c7-121">**Activer**</span><span class="sxs-lookup"><span data-stu-id="ad5c7-121">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="ad5c7-122">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad5c7-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad5c7-123">Suivi d’activation/désactivation.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-123">Track enable/disable.</span></span> <span data-ttu-id="ad5c7-124">Pour activer, affectez à la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-124">To enable, set to **TRUE**.</span></span> <span data-ttu-id="ad5c7-125">Pour désactiver, affectez la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-125">To disable, set to **FALSE**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad5c7-126">Notes</span><span class="sxs-lookup"><span data-stu-id="ad5c7-126">Remarks</span></span>

<span data-ttu-id="ad5c7-127">Les pistes avec la même priorité sont fusionnées ensemble, et les deux valeurs résultantes sont ensuite fusionnées à l’aide du facteur de fusion de priorité.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-127">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span> <span data-ttu-id="ad5c7-128">Une piste doit avoir un ensemble d’animations (stocké séparément) qui lui est associé.</span><span class="sxs-lookup"><span data-stu-id="ad5c7-128">A track must have an animation set (stored separately) associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad5c7-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad5c7-129">Requirements</span></span>



| <span data-ttu-id="ad5c7-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad5c7-130">Requirement</span></span> | <span data-ttu-id="ad5c7-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad5c7-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5c7-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad5c7-132">Header</span></span><br/> | <dl> <span data-ttu-id="ad5c7-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad5c7-133"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad5c7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad5c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad5c7-135">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="ad5c7-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
