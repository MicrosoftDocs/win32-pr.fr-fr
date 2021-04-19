---
description: Effectue une interpolation spline Hermite à l’aide des vecteurs 3D spécifiés.
ms.assetid: d2212299-0478-48a6-b303-60c212528058
title: D3DXVec3Hermite, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b2650bbaf33e5d768ed892bbde31493c8ec0d9d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523832"
---
# <a name="d3dxvec3hermite-function-d3dx10mathh"></a><span data-ttu-id="ba128-103">D3DXVec3Hermite, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ba128-103">D3DXVec3Hermite function (D3DX10Math.h)</span></span>

<span data-ttu-id="ba128-104">Effectue une interpolation spline Hermite à l’aide des vecteurs 3D spécifiés.</span><span class="sxs-lookup"><span data-stu-id="ba128-104">Performs a Hermite spline interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba128-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba128-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Hermite(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pT1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="ba128-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba128-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba128-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ba128-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba128-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba128-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ba128-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ba128-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ba128-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba128-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba128-111">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba128-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ba128-112">Pointeur vers une structure source D3DXVECTOR3, un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="ba128-112">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="ba128-113">*pt1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba128-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba128-114">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba128-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ba128-115">Pointeur vers une structure source D3DXVECTOR3, un vecteur tangent.</span><span class="sxs-lookup"><span data-stu-id="ba128-115">Pointer to a source D3DXVECTOR3 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="ba128-116">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba128-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba128-117">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba128-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ba128-118">Pointeur vers une structure source D3DXVECTOR3, un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="ba128-118">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="ba128-119">*Pt2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba128-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba128-120">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba128-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ba128-121">Pointeur vers une structure source D3DXVECTOR3, un vecteur tangent.</span><span class="sxs-lookup"><span data-stu-id="ba128-121">Pointer to a source D3DXVECTOR3 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="ba128-122"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba128-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba128-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba128-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba128-124">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="ba128-124">Weighting factor.</span></span> <span data-ttu-id="ba128-125">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ba128-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba128-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba128-126">Return value</span></span>

<span data-ttu-id="ba128-127">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba128-127">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ba128-128">Pointeur vers une structure D3DXVECTOR3 qui est le résultat de l’interpolation spline Hermite.</span><span class="sxs-lookup"><span data-stu-id="ba128-128">Pointer to a D3DXVECTOR3 structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba128-129">Notes</span><span class="sxs-lookup"><span data-stu-id="ba128-129">Remarks</span></span>

<span data-ttu-id="ba128-130">La fonction **D3DXVec3Hermite** interpole de (positiona, tangenta) à (PositionB, tangentB) à l’aide de l’interpolation spline Hermite.</span><span class="sxs-lookup"><span data-stu-id="ba128-130">The **D3DXVec3Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="ba128-131">L’interpolation spline est une généralisation de l’accélération et de la simplicité de la spline.</span><span class="sxs-lookup"><span data-stu-id="ba128-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="ba128-132">La rampe est une fonction de Q (s) avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ba128-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="ba128-133">Q (s) = As ³ + BS ² + CS + D (et par conséquent, Q' (s) = 3As ² + 2Bs + C)</span><span class="sxs-lookup"><span data-stu-id="ba128-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="ba128-134">a) Q (0) = v1, Q' (0) = T1</span><span class="sxs-lookup"><span data-stu-id="ba128-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="ba128-135">b) Q (1) = v2, Q' (1) = T2</span><span class="sxs-lookup"><span data-stu-id="ba128-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="ba128-136">v1 est le contenu de pV1, v2 dans le contenu de pV2, T1 est le contenu de pT1, et T2 est le contenu de pT2.</span><span class="sxs-lookup"><span data-stu-id="ba128-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="ba128-137">Ces propriétés sont utilisées pour résoudre A, B, C, D.</span><span class="sxs-lookup"><span data-stu-id="ba128-137">These properties are used to solve for A, B, C, D.</span></span>


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```



<span data-ttu-id="ba128-138">Branchez les solutions pour A, B, C et D pour générer Q (s).</span><span class="sxs-lookup"><span data-stu-id="ba128-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>


```
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```



<span data-ttu-id="ba128-139">Cela donne :</span><span class="sxs-lookup"><span data-stu-id="ba128-139">This yields:</span></span>

<span data-ttu-id="ba128-140">Q (s) = (2V1-2V2 + T2 + T1) s ³ + (3V2-3V1-2t1-T2) s ² + T1S + v1</span><span class="sxs-lookup"><span data-stu-id="ba128-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="ba128-141">Qui peuvent être réorganisés comme suit :</span><span class="sxs-lookup"><span data-stu-id="ba128-141">Which can be rearranged as:</span></span>

<span data-ttu-id="ba128-142">Q (s) = (2S ³-3S ² + 1) v1 + (-2S ³ + 3S ²) v2 + (s ³-2S ² + s) T1 + (s ³-s ²) T2</span><span class="sxs-lookup"><span data-stu-id="ba128-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="ba128-143">Les splines Hermite sont utiles pour le contrôle de l’animation, car la courbe s’exécute à travers tous les points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ba128-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="ba128-144">En outre, étant donné que la position et la tangente sont explicitement spécifiées aux extrémités de chaque segment, il est facile de créer une courbe continue C2 tant que vous vous assurez que votre position de départ et la tangente correspondent aux valeurs de fin du dernier segment.</span><span class="sxs-lookup"><span data-stu-id="ba128-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="ba128-145">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="ba128-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ba128-146">De cette façon, la fonction **D3DXVec3Hermite** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="ba128-146">In this way, the **D3DXVec3Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba128-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba128-147">Requirements</span></span>



| <span data-ttu-id="ba128-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba128-148">Requirement</span></span> | <span data-ttu-id="ba128-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba128-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba128-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba128-150">Header</span></span><br/> | <dl> <span data-ttu-id="ba128-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba128-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba128-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba128-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba128-153">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="ba128-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
