---
description: 'D3DX10_WELD_EPSILONS structure : spécifie des valeurs de tolérance pour chaque composant de vertex lors de la comparaison des vertex pour déterminer s’ils sont suffisamment semblables pour être soudés ensemble.'
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: Structure D3DX10_WELD_EPSILONS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 720a10dbe4b22b69910d88d3c03cea9ded768f1b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105427"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="877ab-103">Structure des Epsilon de \_ soudure d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="877ab-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="877ab-104">Spécifie des valeurs de tolérance pour chaque composant de vertex lors de la comparaison des vertex pour déterminer s’ils sont suffisamment semblables pour être soudés ensemble.</span><span class="sxs-lookup"><span data-stu-id="877ab-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="877ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="877ab-105">Syntax</span></span>


```C++
typedef struct D3DX10_WELD_EPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
```



## <a name="members"></a><span data-ttu-id="877ab-106">Membres</span><span class="sxs-lookup"><span data-stu-id="877ab-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="877ab-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="877ab-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="877ab-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="877ab-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="877ab-109">Position</span><span class="sxs-lookup"><span data-stu-id="877ab-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="877ab-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="877ab-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="877ab-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="877ab-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="877ab-112">Poids de fusion</span><span class="sxs-lookup"><span data-stu-id="877ab-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="877ab-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="877ab-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="877ab-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="877ab-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="877ab-115">Normal</span><span class="sxs-lookup"><span data-stu-id="877ab-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="877ab-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="877ab-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="877ab-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="877ab-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="877ab-118">Valeur de la taille du point</span><span class="sxs-lookup"><span data-stu-id="877ab-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="877ab-119">**Spéculaire**</span><span class="sxs-lookup"><span data-stu-id="877ab-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="877ab-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="877ab-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="877ab-121">Valeur d’éclairage spéculaire</span><span class="sxs-lookup"><span data-stu-id="877ab-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="877ab-122">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="877ab-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="877ab-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="877ab-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="877ab-124">Valeur d’éclairage diffus</span><span class="sxs-lookup"><span data-stu-id="877ab-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="877ab-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="877ab-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="877ab-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="877ab-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="877ab-127">Huit coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="877ab-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="877ab-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="877ab-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="877ab-129">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="877ab-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="877ab-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="877ab-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="877ab-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="877ab-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="877ab-132">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="877ab-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="877ab-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="877ab-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="877ab-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="877ab-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="877ab-135">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="877ab-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="877ab-136">Facteur de pavage</span><span class="sxs-lookup"><span data-stu-id="877ab-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="877ab-137">Notes </span><span class="sxs-lookup"><span data-stu-id="877ab-137">Remarks</span></span>

<span data-ttu-id="877ab-138">Le type LPD3DXWeldEpsilons est défini en tant que pointeur vers la structure D3DXWeldEpsilons.</span><span class="sxs-lookup"><span data-stu-id="877ab-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="877ab-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="877ab-139">Requirements</span></span>



| <span data-ttu-id="877ab-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="877ab-140">Requirement</span></span> | <span data-ttu-id="877ab-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="877ab-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="877ab-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="877ab-142">Header</span></span><br/> | <dl> <span data-ttu-id="877ab-143"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="877ab-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="877ab-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="877ab-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="877ab-145">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="877ab-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
