---
description: Crée une matrice de transformation affine 2D dans le plan XY. Les arguments NULL sont traités comme des transformations d’identité.
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: D3DXMatrixAffineTransformation2D, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6edd0658eb80ec53d19b6c136a672cb78a2087b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532185"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a><span data-ttu-id="97f1e-104">D3DXMatrixAffineTransformation2D, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="97f1e-104">D3DXMatrixAffineTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="97f1e-105">Crée une matrice de transformation affine 2D dans le plan XY.</span><span class="sxs-lookup"><span data-stu-id="97f1e-105">Builds a 2D affine transformation matrix in the xy plane.</span></span> <span data-ttu-id="97f1e-106">Les arguments **null** sont traités comme des transformations d’identité.</span><span class="sxs-lookup"><span data-stu-id="97f1e-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f1e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97f1e-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_          FLOAT       Scaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="97f1e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97f1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97f1e-109">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="97f1e-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97f1e-110">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="97f1e-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="97f1e-111">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="97f1e-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="97f1e-112">*Mise à l’échelle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97f1e-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97f1e-113">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97f1e-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97f1e-114">Facteur d’échelle.</span><span class="sxs-lookup"><span data-stu-id="97f1e-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="97f1e-115">*pRotationCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97f1e-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97f1e-116">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="97f1e-116">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="97f1e-117">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) , point identifiant le centre de rotation.</span><span class="sxs-lookup"><span data-stu-id="97f1e-117">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="97f1e-118">Si cet argument a la **valeur null**, une matrice Identity M <sub>RC</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="97f1e-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="97f1e-119">*Rotation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97f1e-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97f1e-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97f1e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97f1e-121">Angle de rotation.</span><span class="sxs-lookup"><span data-stu-id="97f1e-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="97f1e-122">*pTranslation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97f1e-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97f1e-123">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="97f1e-123">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="97f1e-124">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) représentant la translation.</span><span class="sxs-lookup"><span data-stu-id="97f1e-124">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, representing the translation.</span></span> <span data-ttu-id="97f1e-125">Si cet argument a la **valeur null**, une matrice Identity MT est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="97f1e-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97f1e-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97f1e-126">Return value</span></span>

<span data-ttu-id="97f1e-127">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="97f1e-127">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="97f1e-128">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de transformation affine.</span><span class="sxs-lookup"><span data-stu-id="97f1e-128">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="97f1e-129">Notes</span><span class="sxs-lookup"><span data-stu-id="97f1e-129">Remarks</span></span>

<span data-ttu-id="97f1e-130">Cette fonction calcule la matrice de transformation affine avec la formule suivante, avec la concaténation de matrice évaluée dans l’ordre de gauche à droite :</span><span class="sxs-lookup"><span data-stu-id="97f1e-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="97f1e-131">M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="97f1e-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="97f1e-132">où :</span><span class="sxs-lookup"><span data-stu-id="97f1e-132">where:</span></span>

<span data-ttu-id="97f1e-133">M <sub>out</sub> = matrice de sortie (*moue*)</span><span class="sxs-lookup"><span data-stu-id="97f1e-133">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="97f1e-134">MS = matrice de mise à l’échelle (*mise à l’échelle*)</span><span class="sxs-lookup"><span data-stu-id="97f1e-134">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="97f1e-135">M <sub>RC</sub> = Centre de rotation de la matrice (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="97f1e-135">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="97f1e-136">M <sub>r</sub> = matrice de rotation (*rotation*)</span><span class="sxs-lookup"><span data-stu-id="97f1e-136">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="97f1e-137">MT = matrice de translation (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="97f1e-137">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="97f1e-138">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="97f1e-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="97f1e-139">De cette façon, la fonction **D3DXMatrixAffineTransformation2D** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="97f1e-139">In this way, the **D3DXMatrixAffineTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="97f1e-140">Pour les transformations affines 3D, utilisez [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span><span class="sxs-lookup"><span data-stu-id="97f1e-140">For 3D affine transformations, use [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97f1e-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97f1e-141">Requirements</span></span>



| <span data-ttu-id="97f1e-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97f1e-142">Requirement</span></span> | <span data-ttu-id="97f1e-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="97f1e-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97f1e-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="97f1e-144">Header</span></span><br/>  | <dl> <span data-ttu-id="97f1e-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="97f1e-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="97f1e-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="97f1e-146">Library</span></span><br/> | <dl> <span data-ttu-id="97f1e-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97f1e-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97f1e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97f1e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97f1e-149">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="97f1e-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="97f1e-150">**D3DXMatrixTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="97f1e-150">**D3DXMatrixTransformation2D**</span></span>](d3dxmatrixtransformation2d.md)
</dt> <dt>

[<span data-ttu-id="97f1e-151">Transformations (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="97f1e-151">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
