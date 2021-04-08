---
description: Décrit une intersection de rayons de rayon.
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: Structure D3DX10_INTERSECT_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_INTERSECT_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 87490e734299cba57952bb43d1ee4ffad8e014c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762115"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="ca4b3-103">D3DX10 \_ Intersect ( \_ structure d’informations)</span><span class="sxs-lookup"><span data-stu-id="ca4b3-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="ca4b3-104">Décrit une intersection de rayons de rayon.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca4b3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca4b3-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="ca4b3-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ca4b3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca4b3-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="ca4b3-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="ca4b3-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca4b3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ca4b3-109">Index du triangle qui atteint le rayon.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="ca4b3-110">**U**</span><span class="sxs-lookup"><span data-stu-id="ca4b3-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="ca4b3-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca4b3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ca4b3-112">Coordonnée Barycentric dans le triangle où le rayon croise.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="ca4b3-113">**V**</span><span class="sxs-lookup"><span data-stu-id="ca4b3-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="ca4b3-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca4b3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ca4b3-115">Coordonnée Barycentric dans le triangle où le rayon croise.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="ca4b3-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="ca4b3-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="ca4b3-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca4b3-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ca4b3-118">Distance le long du rayon où l’intersection s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca4b3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ca4b3-119">Remarks</span></span>

<span data-ttu-id="ca4b3-120">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="ca4b3-121">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="ca4b3-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca4b3-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca4b3-122">Requirements</span></span>



| <span data-ttu-id="ca4b3-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca4b3-123">Requirement</span></span> | <span data-ttu-id="ca4b3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca4b3-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ca4b3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca4b3-125">Header</span></span><br/> | <dl> <span data-ttu-id="ca4b3-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca4b3-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca4b3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca4b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca4b3-128">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="ca4b3-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
