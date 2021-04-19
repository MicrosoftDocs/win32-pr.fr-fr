---
description: Décrit une intersection de rayons de rayon.
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: D3DXINTERSECTINFO, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINTERSECTINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 31a98e9a7095e81e962b2996dedb9bdf5871533d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531332"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="b9b7e-103">D3DXINTERSECTINFO, structure</span><span class="sxs-lookup"><span data-stu-id="b9b7e-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="b9b7e-104">Décrit une intersection de rayons de rayon.</span><span class="sxs-lookup"><span data-stu-id="b9b7e-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9b7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9b7e-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="b9b7e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b9b7e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9b7e-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="b9b7e-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="b9b7e-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9b7e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9b7e-109">Index du triangle qui atteint le rayon.</span><span class="sxs-lookup"><span data-stu-id="b9b7e-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="b9b7e-110">**U**</span><span class="sxs-lookup"><span data-stu-id="b9b7e-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="b9b7e-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9b7e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9b7e-112">Coordonnée Barycentric dans le triangle où le rayon croise.</span><span class="sxs-lookup"><span data-stu-id="b9b7e-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="b9b7e-113">**V**</span><span class="sxs-lookup"><span data-stu-id="b9b7e-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="b9b7e-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9b7e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9b7e-115">Coordonnée Barycentric dans le triangle où le rayon croise.</span><span class="sxs-lookup"><span data-stu-id="b9b7e-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="b9b7e-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="b9b7e-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="b9b7e-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9b7e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9b7e-118">Distance le long du rayon où l’intersection s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b9b7e-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9b7e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b9b7e-119">Remarks</span></span>

<span data-ttu-id="b9b7e-120">Les coordonnées Barycentric définissent un point à l’intérieur d’un triangle en termes de sommets du triangle.</span><span class="sxs-lookup"><span data-stu-id="b9b7e-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="b9b7e-121">Pour une description plus détaillée des coordonnées Barycentric, consultez [la description des coordonnées Barycentric de MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="b9b7e-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9b7e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9b7e-122">Requirements</span></span>



| <span data-ttu-id="b9b7e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9b7e-123">Requirement</span></span> | <span data-ttu-id="b9b7e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9b7e-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9b7e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9b7e-125">Header</span></span><br/> | <dl> <span data-ttu-id="b9b7e-126"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9b7e-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9b7e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9b7e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9b7e-128">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="b9b7e-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
