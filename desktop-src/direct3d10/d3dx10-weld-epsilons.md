---
description: Spécifie des valeurs de tolérance pour chaque composant de vertex lors de la comparaison des vertex pour déterminer s’ils sont suffisamment semblables pour être soudés ensemble.
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
ms.openlocfilehash: c72f63e3ecef1fdb193fcaec9220f9768204d099
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542169"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="c5b7c-103">Structure des Epsilon de \_ soudure d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="c5b7c-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="c5b7c-104">Spécifie des valeurs de tolérance pour chaque composant de vertex lors de la comparaison des vertex pour déterminer s’ils sont suffisamment semblables pour être soudés ensemble.</span><span class="sxs-lookup"><span data-stu-id="c5b7c-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5b7c-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="c5b7c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c5b7c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5b7c-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="c5b7c-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5b7c-109">Position</span><span class="sxs-lookup"><span data-stu-id="c5b7c-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="c5b7c-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="c5b7c-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5b7c-112">Poids de fusion</span><span class="sxs-lookup"><span data-stu-id="c5b7c-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="c5b7c-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="c5b7c-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5b7c-115">Normal</span><span class="sxs-lookup"><span data-stu-id="c5b7c-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="c5b7c-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="c5b7c-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5b7c-118">Valeur de la taille du point</span><span class="sxs-lookup"><span data-stu-id="c5b7c-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="c5b7c-119">**Spéculaire**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="c5b7c-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5b7c-121">Valeur d’éclairage spéculaire</span><span class="sxs-lookup"><span data-stu-id="c5b7c-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="c5b7c-122">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="c5b7c-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5b7c-124">Valeur d’éclairage diffus</span><span class="sxs-lookup"><span data-stu-id="c5b7c-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="c5b7c-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="c5b7c-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5b7c-127">Huit coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="c5b7c-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="c5b7c-128">**Tangence**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="c5b7c-129">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5b7c-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="c5b7c-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="c5b7c-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="c5b7c-132">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5b7c-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="c5b7c-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="c5b7c-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="c5b7c-135">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5b7c-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5b7c-136">Facteur de pavage</span><span class="sxs-lookup"><span data-stu-id="c5b7c-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5b7c-137">Notes</span><span class="sxs-lookup"><span data-stu-id="c5b7c-137">Remarks</span></span>

<span data-ttu-id="c5b7c-138">Le type LPD3DXWeldEpsilons est défini en tant que pointeur vers la structure D3DXWeldEpsilons.</span><span class="sxs-lookup"><span data-stu-id="c5b7c-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="c5b7c-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5b7c-139">Requirements</span></span>



| <span data-ttu-id="c5b7c-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5b7c-140">Requirement</span></span> | <span data-ttu-id="c5b7c-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5b7c-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b7c-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5b7c-142">Header</span></span><br/> | <dl> <span data-ttu-id="c5b7c-143"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5b7c-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5b7c-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5b7c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b7c-145">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="c5b7c-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
