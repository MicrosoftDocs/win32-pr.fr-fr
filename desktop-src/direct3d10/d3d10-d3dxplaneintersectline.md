---
description: Recherche l’intersection entre un plan et une ligne.
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: D3DXPlaneIntersectLine, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00d25fcba9e5884cec10da96964ad0f5daa9ed14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106533717"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a><span data-ttu-id="770f9-103">D3DXPlaneIntersectLine, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="770f9-103">D3DXPlaneIntersectLine function (D3DX10Math.h)</span></span>

<span data-ttu-id="770f9-104">Recherche l’intersection entre un plan et une ligne.</span><span class="sxs-lookup"><span data-stu-id="770f9-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="770f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="770f9-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="770f9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="770f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="770f9-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="770f9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="770f9-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="770f9-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="770f9-109">Pointeur vers un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifiant l’intersection entre le plan et la ligne spécifiés.</span><span class="sxs-lookup"><span data-stu-id="770f9-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="770f9-110">*pp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="770f9-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="770f9-111">Type : **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="770f9-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="770f9-112">Pointeur vers le [**D3DXPLANE**](d3d10-d3dxplane.md)source.</span><span class="sxs-lookup"><span data-stu-id="770f9-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> <dt>

<span data-ttu-id="770f9-113">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="770f9-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="770f9-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="770f9-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="770f9-115">Pointeur vers une structure D3DXVECTOR3 source, définissant un point de départ de ligne.</span><span class="sxs-lookup"><span data-stu-id="770f9-115">Pointer to a source D3DXVECTOR3 structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="770f9-116">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="770f9-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="770f9-117">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="770f9-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="770f9-118">Pointeur vers une structure D3DXVECTOR3 source, définissant un point de fin de ligne.</span><span class="sxs-lookup"><span data-stu-id="770f9-118">Pointer to a source D3DXVECTOR3 structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="770f9-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="770f9-119">Return value</span></span>

<span data-ttu-id="770f9-120">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="770f9-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="770f9-121">Pointeur vers une structure D3DXVECTOR3 qui est l’intersection entre le plan et la ligne spécifiés.</span><span class="sxs-lookup"><span data-stu-id="770f9-121">Pointer to a D3DXVECTOR3 structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="770f9-122">Notes</span><span class="sxs-lookup"><span data-stu-id="770f9-122">Remarks</span></span>

<span data-ttu-id="770f9-123">Si la ligne est parallèle au plan, la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="770f9-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="770f9-124">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="770f9-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="770f9-125">De cette façon, la fonction D3DXPlaneIntersectLine peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="770f9-125">In this way, the D3DXPlaneIntersectLine function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="770f9-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="770f9-126">Requirements</span></span>



| <span data-ttu-id="770f9-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="770f9-127">Requirement</span></span> | <span data-ttu-id="770f9-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="770f9-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="770f9-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="770f9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="770f9-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="770f9-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="770f9-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="770f9-131">Library</span></span><br/> | <dl> <span data-ttu-id="770f9-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="770f9-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="770f9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="770f9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="770f9-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="770f9-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
