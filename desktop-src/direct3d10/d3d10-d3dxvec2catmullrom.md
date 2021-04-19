---
description: Effectue une interpolation Catmull-Rom à l’aide des vecteurs 2D spécifiés.
ms.assetid: 8ec1abfa-0fa9-486a-b86d-bbb8f1d63849
title: D3DXVec2CatmullRom, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CatmullRom
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 71f499313a31c200b5cc657664b10b43dde47ba6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529625"
---
# <a name="d3dxvec2catmullrom-function-d3dx10mathh"></a><span data-ttu-id="d4d53-103">D3DXVec2CatmullRom, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d4d53-103">D3DXVec2CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="d4d53-104">Effectue une interpolation Catmull-Rom à l’aide des vecteurs 2D spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d4d53-104">Performs a Catmull-Rom interpolation, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d53-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4d53-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2CatmullRom(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV0,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="d4d53-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4d53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d53-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d4d53-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d53-108">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4d53-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d4d53-109">Pointeur vers le [**D3DXVECTOR2**](d3d10-d3dxvector2.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d4d53-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4d53-110">*pV0* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4d53-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d53-111">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4d53-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d4d53-112">Pointeur vers une structure source D3DXVECTOR2, un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="d4d53-112">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="d4d53-113">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4d53-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d53-114">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4d53-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d4d53-115">Pointeur vers une structure source D3DXVECTOR2, un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="d4d53-115">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="d4d53-116">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4d53-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d53-117">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4d53-117">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d4d53-118">Pointeur vers une structure source D3DXVECTOR2, un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="d4d53-118">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="d4d53-119">*pV3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4d53-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d53-120">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4d53-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d4d53-121">Pointeur vers une structure source D3DXVECTOR2, un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="d4d53-121">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="d4d53-122"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4d53-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d53-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4d53-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4d53-124">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="d4d53-124">Weighting factor.</span></span> <span data-ttu-id="d4d53-125">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="d4d53-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4d53-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4d53-126">Return value</span></span>

<span data-ttu-id="d4d53-127">Type : **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4d53-127">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d4d53-128">Pointeur vers une structure D3DXVECTOR2 qui est le résultat de l’interpolation Catmull-Rom.</span><span class="sxs-lookup"><span data-stu-id="d4d53-128">Pointer to a D3DXVECTOR2 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d53-129">Notes</span><span class="sxs-lookup"><span data-stu-id="d4d53-129">Remarks</span></span>

<span data-ttu-id="d4d53-130">À partir de quatre points (P1, P2, P3, P4), recherchez une fonction Q (s) de ce type :</span><span class="sxs-lookup"><span data-stu-id="d4d53-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="d4d53-131">Le Catmull-Rom spline peut être dérivé de la spline Hermite en définissant :</span><span class="sxs-lookup"><span data-stu-id="d4d53-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="d4d53-132">où :</span><span class="sxs-lookup"><span data-stu-id="d4d53-132">where:</span></span>

<span data-ttu-id="d4d53-133">v1 est le contenu de pV0.</span><span class="sxs-lookup"><span data-stu-id="d4d53-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="d4d53-134">v2 est le contenu de pV1.</span><span class="sxs-lookup"><span data-stu-id="d4d53-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="d4d53-135">P3 est le contenu de pV2.</span><span class="sxs-lookup"><span data-stu-id="d4d53-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="d4d53-136">P4 est le contenu de pV3.</span><span class="sxs-lookup"><span data-stu-id="d4d53-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="d4d53-137">À l’aide de l’équation spline Hermite :</span><span class="sxs-lookup"><span data-stu-id="d4d53-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="d4d53-138">et le remplacement de v1, v2, T1, T2 donne :</span><span class="sxs-lookup"><span data-stu-id="d4d53-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2)/2
```



<span data-ttu-id="d4d53-139">Cette réorganisation peut être réorganisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="d4d53-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="d4d53-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4d53-140">Requirements</span></span>



| <span data-ttu-id="d4d53-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4d53-141">Requirement</span></span> | <span data-ttu-id="d4d53-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d53-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d53-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4d53-143">Header</span></span><br/>  | <dl> <span data-ttu-id="d4d53-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d53-144"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d4d53-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4d53-145">Library</span></span><br/> | <dl> <span data-ttu-id="d4d53-146"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4d53-146"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4d53-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4d53-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d53-148">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d4d53-148">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
