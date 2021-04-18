---
description: Crée une matrice de transformation affine 2D dans le plan x-y. Les arguments NULL sont traités comme des transformations d’identité.
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: D3DXMatrixAffineTransformation2D, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 223ef5d2d9a68c993553d52f5d4cf63e8b95dd3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523227"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a><span data-ttu-id="1eeb2-104">D3DXMatrixAffineTransformation2D, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1eeb2-104">D3DXMatrixAffineTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="1eeb2-105">Crée une matrice de transformation affine 2D dans le plan x-y.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-105">Builds a 2D affine transformation matrix in the x-y plane.</span></span> <span data-ttu-id="1eeb2-106">Les arguments **null** sont traités comme des transformations d’identité.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eeb2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eeb2-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _In_       D3DXMATRIX  *pOut,
  _In_       FLOAT       Scaling,
  _In_ const D3DXVECTOR2 *pRotationCenter,
  _In_       FLOAT       Rotation,
  _In_ const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="1eeb2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1eeb2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eeb2-109">*moue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eeb2-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeb2-110">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eeb2-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1eeb2-111">Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1eeb2-112">*Mise à l’échelle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eeb2-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeb2-113">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eeb2-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eeb2-114">Facteur d’échelle.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="1eeb2-115">*pRotationCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eeb2-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeb2-116">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eeb2-116">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1eeb2-117">Pointeur vers un [**D3DXVECTOR2**](d3d10-d3dxvector2.md), point identifiant le centre de rotation.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-117">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="1eeb2-118">Si cet argument a la **valeur null**, une matrice Identity M <sub>RC</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1eeb2-119">*Rotation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eeb2-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeb2-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eeb2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eeb2-121">Angle de rotation.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="1eeb2-122">*pTranslation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eeb2-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeb2-123">Type : **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eeb2-123">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1eeb2-124">Pointeur vers un [**D3DXVECTOR2**](d3d10-d3dxvector2.md)qui représente la translation.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-124">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), representing the translation.</span></span> <span data-ttu-id="1eeb2-125">Si cet argument a la **valeur null**, une matrice Identity MT est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eeb2-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1eeb2-126">Return value</span></span>

<span data-ttu-id="1eeb2-127">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eeb2-127">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1eeb2-128">Pointeur vers une structure D3DXMATRIX qui est une matrice de transformation affine.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-128">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eeb2-129">Notes</span><span class="sxs-lookup"><span data-stu-id="1eeb2-129">Remarks</span></span>

<span data-ttu-id="1eeb2-130">Cette fonction calcule la matrice de transformation affine avec la formule suivante, avec la concaténation de matrice évaluée dans l’ordre de gauche à droite :</span><span class="sxs-lookup"><span data-stu-id="1eeb2-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="1eeb2-131">M<sub>out</sub> = MS \* (m<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="1eeb2-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="1eeb2-132">où :</span><span class="sxs-lookup"><span data-stu-id="1eeb2-132">where:</span></span>

<span data-ttu-id="1eeb2-133">M<sub>out</sub> = matrice de sortie (moue)</span><span class="sxs-lookup"><span data-stu-id="1eeb2-133">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="1eeb2-134">MS = matrice de mise à l’échelle (mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="1eeb2-134">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="1eeb2-135">M<sub>RC</sub> = Centre de rotation de la matrice (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="1eeb2-135">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="1eeb2-136">M<sub>r</sub> = matrice de rotation (rotation)</span><span class="sxs-lookup"><span data-stu-id="1eeb2-136">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="1eeb2-137">MT = matrice de translation (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="1eeb2-137">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="1eeb2-138">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1eeb2-139">De cette façon, la fonction D3DXMatrixAffineTransformation2D peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-139">In this way, the D3DXMatrixAffineTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1eeb2-140">Pour les transformations affines 3D, utilisez D3DXMatrixAffineTransformation.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-140">For 3D affine transformations, use D3DXMatrixAffineTransformation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eeb2-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1eeb2-141">Requirements</span></span>



| <span data-ttu-id="1eeb2-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eeb2-142">Requirement</span></span> | <span data-ttu-id="1eeb2-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eeb2-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eeb2-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="1eeb2-144">Header</span></span><br/>  | <dl> <span data-ttu-id="1eeb2-145"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eeb2-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1eeb2-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1eeb2-146">Library</span></span><br/> | <dl> <span data-ttu-id="1eeb2-147"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1eeb2-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1eeb2-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eeb2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eeb2-149">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="1eeb2-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
