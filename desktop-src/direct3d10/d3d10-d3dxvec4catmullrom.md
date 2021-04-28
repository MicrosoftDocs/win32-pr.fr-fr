---
description: D3DXVec4CatmullRom, fonction (D3DX10Math. h)-effectue une interpolation Catmull-Rom à l’aide des vecteurs 4D spécifiés.
ms.assetid: e3a10989-e25e-46fa-b72e-bade936cacf1
title: D3DXVec4CatmullRom, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 4e3665709564f578046273facbd3311253d8c2b9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102957"
---
# <a name="d3dxvec4catmullrom-function-d3dx10mathh"></a><span data-ttu-id="5f561-103">D3DXVec4CatmullRom, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5f561-103">D3DXVec4CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="5f561-104">Effectue une interpolation Catmull-Rom à l’aide des vecteurs 4D spécifiés.</span><span class="sxs-lookup"><span data-stu-id="5f561-104">Performs a Catmull-Rom interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f561-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f561-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="5f561-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f561-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f561-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5f561-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f561-108">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f561-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="5f561-109">Pointeur vers le [**D3DXVECTOR4**](d3d10-d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5f561-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5f561-110">*pV0* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f561-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f561-111">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f561-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="5f561-112">Pointeur vers une structure source D3DXVECTOR4, un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="5f561-112">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="5f561-113">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f561-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f561-114">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f561-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="5f561-115">Pointeur vers une structure source D3DXVECTOR4, un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="5f561-115">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="5f561-116">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f561-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f561-117">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f561-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="5f561-118">Pointeur vers une structure source D3DXVECTOR4, un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="5f561-118">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="5f561-119">*pV3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f561-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f561-120">Type : **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f561-120">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="5f561-121">Pointeur vers une structure source D3DXVECTOR4, un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="5f561-121">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="5f561-122"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f561-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f561-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f561-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f561-124">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="5f561-124">Weighting factor.</span></span> <span data-ttu-id="5f561-125">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5f561-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f561-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5f561-126">Return value</span></span>

<span data-ttu-id="5f561-127">Type : **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f561-127">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="5f561-128">Pointeur vers une structure D3DXVECTOR4 qui est le résultat de l’interpolation Catmull-Rom.</span><span class="sxs-lookup"><span data-stu-id="5f561-128">Pointer to a D3DXVECTOR4 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f561-129">Notes </span><span class="sxs-lookup"><span data-stu-id="5f561-129">Remarks</span></span>

<span data-ttu-id="5f561-130">À partir de quatre points (P1, P2, P3, P4), recherchez une fonction Q (s) de ce type :</span><span class="sxs-lookup"><span data-stu-id="5f561-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="5f561-131">Le Catmull-Rom spline peut être dérivé de la spline Hermite en définissant :</span><span class="sxs-lookup"><span data-stu-id="5f561-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="5f561-132">où :</span><span class="sxs-lookup"><span data-stu-id="5f561-132">where:</span></span>

<span data-ttu-id="5f561-133">v1 est le contenu de pV0.</span><span class="sxs-lookup"><span data-stu-id="5f561-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="5f561-134">v2 dans le contenu de pV1.</span><span class="sxs-lookup"><span data-stu-id="5f561-134">v2 in the contents of pV1.</span></span>

<span data-ttu-id="5f561-135">P3 est le contenu de pV2.</span><span class="sxs-lookup"><span data-stu-id="5f561-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="5f561-136">P4 est le contenu de pV3.</span><span class="sxs-lookup"><span data-stu-id="5f561-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="5f561-137">À l’aide de l’équation spline Hermite :</span><span class="sxs-lookup"><span data-stu-id="5f561-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="5f561-138">et le remplacement de v1, v2, T1, T2 donne :</span><span class="sxs-lookup"><span data-stu-id="5f561-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="5f561-139">Cette réorganisation peut être réorganisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="5f561-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="5f561-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f561-140">Requirements</span></span>



| <span data-ttu-id="5f561-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f561-141">Requirement</span></span> | <span data-ttu-id="5f561-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f561-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f561-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f561-143">Header</span></span><br/> | <dl> <span data-ttu-id="5f561-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f561-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f561-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f561-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f561-146">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="5f561-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
