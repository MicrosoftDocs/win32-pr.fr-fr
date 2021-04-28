---
description: Fonction D3DXVec4Hermite (D3dx9math. h)-effectue une interpolation spline Hermite à l’aide des vecteurs 4D spécifiés.
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: D3DXVec4Hermite, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08ed785c24ba9580be0fc7f620a471ea96184a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097697"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a><span data-ttu-id="2a047-103">D3DXVec4Hermite, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2a047-103">D3DXVec4Hermite function (D3dx9math.h)</span></span>

<span data-ttu-id="2a047-104">Effectue une interpolation spline Hermite à l’aide des vecteurs 4D spécifiés.</span><span class="sxs-lookup"><span data-stu-id="2a047-104">Performs a Hermite spline interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a047-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a047-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Hermite(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pT1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="2a047-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a047-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2a047-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a047-108">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a047-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2a047-109">Pointeur vers la structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2a047-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-110">*pV1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a047-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a047-111">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a047-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2a047-112">Pointeur vers une structure source [**D3DXVECTOR4**](d3dxvector4.md) , un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="2a047-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-113">*pt1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a047-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a047-114">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a047-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2a047-115">Pointeur vers une structure source [**D3DXVECTOR4**](d3dxvector4.md) , un vecteur tangent.</span><span class="sxs-lookup"><span data-stu-id="2a047-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-116">*pV2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a047-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a047-117">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a047-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2a047-118">Pointeur vers une structure source [**D3DXVECTOR4**](d3dxvector4.md) , un vecteur de position.</span><span class="sxs-lookup"><span data-stu-id="2a047-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-119">*Pt2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a047-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a047-120">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a047-120">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2a047-121">Pointeur vers une structure source [**D3DXVECTOR4**](d3dxvector4.md) , un vecteur tangent.</span><span class="sxs-lookup"><span data-stu-id="2a047-121">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-122"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a047-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a047-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a047-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a047-124">Facteur de pondération.</span><span class="sxs-lookup"><span data-stu-id="2a047-124">Weighting factor.</span></span> <span data-ttu-id="2a047-125">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="2a047-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a047-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2a047-126">Return value</span></span>

<span data-ttu-id="2a047-127">Type : **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a047-127">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2a047-128">Pointeur vers une structure [**D3DXVECTOR4**](d3dxvector4.md) qui est le résultat de l’interpolation spline Hermite.</span><span class="sxs-lookup"><span data-stu-id="2a047-128">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a047-129">Notes </span><span class="sxs-lookup"><span data-stu-id="2a047-129">Remarks</span></span>

<span data-ttu-id="2a047-130">La fonction **D3DXVec4Hermite** interpole de (positiona, tangenta) à (PositionB, tangentB) à l’aide de l’interpolation spline Hermite.</span><span class="sxs-lookup"><span data-stu-id="2a047-130">The **D3DXVec4Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="2a047-131">L’interpolation spline est une généralisation de l’accélération et de la simplicité de la spline.</span><span class="sxs-lookup"><span data-stu-id="2a047-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="2a047-132">La rampe est une fonction de Q (s) avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2a047-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="2a047-133">Q (s) = As ³ + BS ² + CS + D (et par conséquent, Q' (s) = 3As ² + 2Bs + C)</span><span class="sxs-lookup"><span data-stu-id="2a047-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="2a047-134">a) Q (0) = v1, Q' (0) = T1</span><span class="sxs-lookup"><span data-stu-id="2a047-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="2a047-135">b) Q (1) = v2, Q' (1) = T2</span><span class="sxs-lookup"><span data-stu-id="2a047-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="2a047-136">v1 est le contenu de pV1, v2 dans le contenu de pV2, T1 est le contenu de pT1, et T2 est le contenu de pT2.</span><span class="sxs-lookup"><span data-stu-id="2a047-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="2a047-137">Ces propriétés sont utilisées pour résoudre A, B, C, D.</span><span class="sxs-lookup"><span data-stu-id="2a047-137">These properties are used to solve for A, B, C, D.</span></span>

<span data-ttu-id="2a047-138">Branchez les solutions pour A, B, C et D pour générer Q (s).</span><span class="sxs-lookup"><span data-stu-id="2a047-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

<span data-ttu-id="2a047-139">Cela donne :</span><span class="sxs-lookup"><span data-stu-id="2a047-139">This yields:</span></span>

<span data-ttu-id="2a047-140">Q (s) = (2V1-2V2 + T2 + T1) s ³ + (3V2-3V1-2t1-T2) s ² + T1S + v1</span><span class="sxs-lookup"><span data-stu-id="2a047-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="2a047-141">Qui peuvent être réorganisés comme suit :</span><span class="sxs-lookup"><span data-stu-id="2a047-141">Which can be rearranged as:</span></span>

<span data-ttu-id="2a047-142">Q (s) = (2S ³-3S ² + 1) v1 + (-2S ³ + 3S ²) v2 + (s ³-2S ² + s) T1 + (s ³-s ²) T2</span><span class="sxs-lookup"><span data-stu-id="2a047-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="2a047-143">Les splines Hermite sont utiles pour le contrôle de l’animation, car la courbe s’exécute à travers tous les points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2a047-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="2a047-144">En outre, étant donné que la position et la tangente sont explicitement spécifiées aux extrémités de chaque segment, il est facile de créer une courbe continue C2 tant que vous vous assurez que votre position de départ et la tangente correspondent aux valeurs de fin du dernier segment.</span><span class="sxs-lookup"><span data-stu-id="2a047-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="2a047-145">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="2a047-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2a047-146">De cette façon, la fonction **D3DXVec4Hermite** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="2a047-146">In this way, the **D3DXVec4Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a047-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a047-147">Requirements</span></span>



| <span data-ttu-id="2a047-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a047-148">Requirement</span></span> | <span data-ttu-id="2a047-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a047-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a047-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a047-150">Header</span></span><br/>  | <dl> <span data-ttu-id="2a047-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a047-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2a047-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2a047-152">Library</span></span><br/> | <dl> <span data-ttu-id="2a047-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a047-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a047-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a047-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a047-155">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="2a047-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
