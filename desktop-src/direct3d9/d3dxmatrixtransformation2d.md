---
description: Crée une matrice de transformation 2D qui représente des transformations dans le plan XY. Les arguments NULL sont traités comme des transformations d’identité.
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: D3DXMatrixTransformation2D, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ead4d403917b5328776b33563bc477c28983d6ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532440"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a><span data-ttu-id="54881-104">D3DXMatrixTransformation2D, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="54881-104">D3DXMatrixTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="54881-105">Crée une matrice de transformation 2D qui représente des transformations dans le plan XY.</span><span class="sxs-lookup"><span data-stu-id="54881-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="54881-106">Les arguments **null** sont traités comme des transformations d’identité.</span><span class="sxs-lookup"><span data-stu-id="54881-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="54881-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54881-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="54881-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54881-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54881-109">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="54881-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54881-110">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="54881-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54881-111">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui contient le résultat des transformations.</span><span class="sxs-lookup"><span data-stu-id="54881-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="54881-112">*pScalingCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54881-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54881-113">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="54881-113">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="54881-114">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) , point identifiant le centre de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="54881-114">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scaling center.</span></span> <span data-ttu-id="54881-115">Si cet argument a la **valeur null**, une matrice Identity M <sub>SC</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="54881-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="54881-116">*pScalingRotation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54881-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54881-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54881-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54881-118">Facteur de rotation de la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="54881-118">The scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="54881-119">*pScaling* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54881-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54881-120">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="54881-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="54881-121">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) , point identifiant l’échelle.</span><span class="sxs-lookup"><span data-stu-id="54881-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scale.</span></span> <span data-ttu-id="54881-122">Si cet argument a la **valeur null**, une matrice d’identité MS est appliquée à la formule dans les notes.</span><span class="sxs-lookup"><span data-stu-id="54881-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="54881-123">*pRotationCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54881-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54881-124">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="54881-124">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="54881-125">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) , point identifiant le centre de rotation.</span><span class="sxs-lookup"><span data-stu-id="54881-125">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the rotation center.</span></span> <span data-ttu-id="54881-126">Si cet argument a la **valeur null**, une matrice Identity M <sub>RC</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="54881-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="54881-127">*Rotation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54881-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54881-128">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54881-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54881-129">Angle de rotation en radians.</span><span class="sxs-lookup"><span data-stu-id="54881-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="54881-130">*pTranslation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54881-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54881-131">Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="54881-131">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="54881-132">Pointeur vers une structure [**D3DXVECTOR2**](d3dxvector2.md) , identifiant la traduction.</span><span class="sxs-lookup"><span data-stu-id="54881-132">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, identifying the translation.</span></span> <span data-ttu-id="54881-133">Si cet argument a la **valeur null**, une matrice Identity MT est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="54881-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54881-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54881-134">Return value</span></span>

<span data-ttu-id="54881-135">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="54881-135">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54881-136">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui contient la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="54881-136">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="54881-137">Notes</span><span class="sxs-lookup"><span data-stu-id="54881-137">Remarks</span></span>

<span data-ttu-id="54881-138">Cette fonction calcule la matrice de transformation avec la formule suivante, avec la concaténation de matrice évaluée dans l’ordre de gauche à droite :</span><span class="sxs-lookup"><span data-stu-id="54881-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="54881-139">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="54881-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="54881-140">où :</span><span class="sxs-lookup"><span data-stu-id="54881-140">where:</span></span>

<span data-ttu-id="54881-141">M <sub>out</sub> = matrice de sortie (*moue*)</span><span class="sxs-lookup"><span data-stu-id="54881-141">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="54881-142">M <sub>SC</sub> = matrice du centre de mise à l’échelle (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="54881-142">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="54881-143">M <sub>SR</sub> = matrice de rotation de la mise à l’échelle (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="54881-143">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="54881-144">MS = matrice de mise à l’échelle (*pScaling*)</span><span class="sxs-lookup"><span data-stu-id="54881-144">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="54881-145">M <sub>RC</sub> = Centre de rotation de la matrice (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="54881-145">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="54881-146">M <sub>r</sub> = matrice de rotation (*rotation*)</span><span class="sxs-lookup"><span data-stu-id="54881-146">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="54881-147">MT = matrice de translation (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="54881-147">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="54881-148">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="54881-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="54881-149">De cette façon, la fonction **D3DXMatrixTransformation2D** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="54881-149">In this way, the **D3DXMatrixTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="54881-150">Pour les transformations 3D, utilisez [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="54881-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54881-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54881-151">Requirements</span></span>



| <span data-ttu-id="54881-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54881-152">Requirement</span></span> | <span data-ttu-id="54881-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="54881-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54881-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="54881-154">Header</span></span><br/>  | <dl> <span data-ttu-id="54881-155"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="54881-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="54881-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54881-156">Library</span></span><br/> | <dl> <span data-ttu-id="54881-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54881-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54881-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54881-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54881-159">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="54881-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="54881-160">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="54881-160">**D3DXMatrixAffineTransformation2D**</span></span>](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[<span data-ttu-id="54881-161">Transformations (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="54881-161">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
