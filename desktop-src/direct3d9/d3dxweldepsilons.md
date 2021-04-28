---
description: 'Structure D3DXWELDEPSILONS : spécifie les valeurs de tolérance pour chaque composant de vertex lors de la comparaison des vertex pour déterminer s’ils sont suffisamment similaires pour être soudés ensemble.'
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: D3DXWELDEPSILONS, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: bb11e6f5481b1adf7cc1bac58edf40d4ac770e92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115497"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="a95be-103">D3DXWELDEPSILONS, structure</span><span class="sxs-lookup"><span data-stu-id="a95be-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="a95be-104">Spécifie des valeurs de tolérance pour chaque composant de vertex lors de la comparaison des vertex pour déterminer s’ils sont suffisamment semblables pour être soudés ensemble.</span><span class="sxs-lookup"><span data-stu-id="a95be-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="a95be-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a95be-105">Syntax</span></span>


```C++
typedef struct _D3DXWELDEPSILONS {
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
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a><span data-ttu-id="a95be-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a95be-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a95be-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="a95be-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="a95be-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a95be-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a95be-109">Position</span><span class="sxs-lookup"><span data-stu-id="a95be-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="a95be-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="a95be-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="a95be-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a95be-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a95be-112">Poids de fusion</span><span class="sxs-lookup"><span data-stu-id="a95be-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="a95be-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="a95be-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="a95be-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a95be-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a95be-115">Normal</span><span class="sxs-lookup"><span data-stu-id="a95be-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="a95be-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="a95be-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="a95be-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a95be-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a95be-118">Valeur de la taille du point</span><span class="sxs-lookup"><span data-stu-id="a95be-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="a95be-119">**Spéculaire**</span><span class="sxs-lookup"><span data-stu-id="a95be-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="a95be-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a95be-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a95be-121">Valeur d’éclairage spéculaire</span><span class="sxs-lookup"><span data-stu-id="a95be-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="a95be-122">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="a95be-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="a95be-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a95be-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a95be-124">Valeur d’éclairage diffus</span><span class="sxs-lookup"><span data-stu-id="a95be-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="a95be-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="a95be-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="a95be-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a95be-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a95be-127">Huit coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="a95be-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="a95be-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="a95be-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="a95be-129">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a95be-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a95be-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="a95be-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="a95be-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="a95be-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="a95be-132">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a95be-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a95be-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="a95be-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="a95be-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="a95be-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="a95be-135">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a95be-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a95be-136">Facteur de pavage</span><span class="sxs-lookup"><span data-stu-id="a95be-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a95be-137">Notes </span><span class="sxs-lookup"><span data-stu-id="a95be-137">Remarks</span></span>

<span data-ttu-id="a95be-138">Le type LPD3DXWELDEPSILONS est défini en tant que pointeur vers la structure **D3DXWELDEPSILONS** .</span><span class="sxs-lookup"><span data-stu-id="a95be-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="a95be-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a95be-139">Requirements</span></span>



| <span data-ttu-id="a95be-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a95be-140">Requirement</span></span> | <span data-ttu-id="a95be-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="a95be-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a95be-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="a95be-142">Header</span></span><br/> | <dl> <span data-ttu-id="a95be-143"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a95be-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a95be-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a95be-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a95be-145">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="a95be-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="a95be-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="a95be-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
