---
description: 'D3DXMatrixTransformation, fonction (D3dx9math. h) : génère une matrice de transformation. Les arguments NULL sont traités comme des transformations d’identité.'
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: D3DXMatrixTransformation, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc3b6502a8015564207f208166cec15227d3b18a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098127"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="1bcda-104">D3DXMatrixTransformation, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1bcda-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="1bcda-105">Crée une matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="1bcda-105">Builds a transformation matrix.</span></span> <span data-ttu-id="1bcda-106">Les arguments **null** sont traités comme des transformations d’identité.</span><span class="sxs-lookup"><span data-stu-id="1bcda-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bcda-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bcda-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="1bcda-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bcda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bcda-109">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1bcda-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bcda-110">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bcda-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1bcda-111">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1bcda-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1bcda-112">*pScalingCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bcda-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bcda-113">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bcda-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1bcda-114">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , identifiant le point central du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="1bcda-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="1bcda-115">Si cet argument a la **valeur null**, une matrice Identity M <sub>SC</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1bcda-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1bcda-116">*pScalingRotation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bcda-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bcda-117">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bcda-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1bcda-118">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui spécifie la rotation de la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="1bcda-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="1bcda-119">Si cet argument a la **valeur null**, une matrice Identity M <sub>SR</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1bcda-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1bcda-120">*pScaling* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bcda-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bcda-121">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bcda-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1bcda-122">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , le vecteur de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="1bcda-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="1bcda-123">Si cet argument a la **valeur null**, une matrice d’identité MS est appliquée à la formule dans les notes.</span><span class="sxs-lookup"><span data-stu-id="1bcda-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1bcda-124">*pRotationCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bcda-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bcda-125">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bcda-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1bcda-126">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , un point qui identifie le centre de rotation.</span><span class="sxs-lookup"><span data-stu-id="1bcda-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="1bcda-127">Si cet argument a la **valeur null**, une matrice Identity M <sub>RC</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1bcda-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1bcda-128">*protique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bcda-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bcda-129">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bcda-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1bcda-130">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui spécifie la rotation.</span><span class="sxs-lookup"><span data-stu-id="1bcda-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="1bcda-131">Si cet argument a la **valeur null**, une matrice Identity M <sub>r</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1bcda-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1bcda-132">*pTranslation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bcda-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bcda-133">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bcda-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1bcda-134">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) représentant la translation.</span><span class="sxs-lookup"><span data-stu-id="1bcda-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="1bcda-135">Si cet argument a la **valeur null**, une matrice Identity MT est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1bcda-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bcda-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bcda-136">Return value</span></span>

<span data-ttu-id="1bcda-137">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bcda-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1bcda-138">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="1bcda-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bcda-139">Notes </span><span class="sxs-lookup"><span data-stu-id="1bcda-139">Remarks</span></span>

<span data-ttu-id="1bcda-140">Cette fonction calcule la matrice de transformation avec la formule suivante, avec la concaténation de matrice évaluée dans l’ordre de gauche à droite :</span><span class="sxs-lookup"><span data-stu-id="1bcda-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="1bcda-141">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="1bcda-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="1bcda-142">où :</span><span class="sxs-lookup"><span data-stu-id="1bcda-142">where:</span></span>

<span data-ttu-id="1bcda-143">M <sub>out</sub> = matrice de sortie (*moue*)</span><span class="sxs-lookup"><span data-stu-id="1bcda-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="1bcda-144">M <sub>SC</sub> = matrice du centre de mise à l’échelle (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="1bcda-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="1bcda-145">M <sub>SR</sub> = matrice de rotation de la mise à l’échelle (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="1bcda-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="1bcda-146">MS = matrice de mise à l’échelle (*pScaling*)</span><span class="sxs-lookup"><span data-stu-id="1bcda-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="1bcda-147">M <sub>RC</sub> = Centre de rotation de la matrice (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="1bcda-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="1bcda-148">M <sub>r</sub> = matrice de rotation (*protique*)</span><span class="sxs-lookup"><span data-stu-id="1bcda-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="1bcda-149">MT = matrice de translation (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="1bcda-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="1bcda-150">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="1bcda-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1bcda-151">De cette façon, la fonction **D3DXMatrixTransformation** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="1bcda-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1bcda-152">Pour les transformations 2D, utilisez [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="1bcda-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bcda-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bcda-153">Requirements</span></span>



| <span data-ttu-id="1bcda-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bcda-154">Requirement</span></span> | <span data-ttu-id="1bcda-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bcda-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bcda-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bcda-156">Header</span></span><br/>  | <dl> <span data-ttu-id="1bcda-157"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bcda-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1bcda-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1bcda-158">Library</span></span><br/> | <dl> <span data-ttu-id="1bcda-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bcda-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bcda-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bcda-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bcda-161">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="1bcda-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1bcda-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="1bcda-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="1bcda-163">Transformations (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1bcda-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




