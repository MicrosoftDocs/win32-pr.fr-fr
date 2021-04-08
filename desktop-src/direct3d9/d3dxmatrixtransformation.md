---
description: Crée une matrice de transformation. Les arguments NULL sont traités comme des transformations d’identité.
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
ms.openlocfilehash: f2174329e01e3e624ef27608ca56b33181b770db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043082"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="4c6c8-104">D3DXMatrixTransformation, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4c6c8-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="4c6c8-105">Crée une matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-105">Builds a transformation matrix.</span></span> <span data-ttu-id="4c6c8-106">Les arguments **null** sont traités comme des transformations d’identité.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c6c8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c6c8-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4c6c8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c6c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c6c8-109">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4c6c8-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6c8-110">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c6c8-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4c6c8-111">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4c6c8-112">*pScalingCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c6c8-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6c8-113">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c6c8-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4c6c8-114">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , identifiant le point central du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="4c6c8-115">Si cet argument a la **valeur null**, une matrice Identity M <sub>SC</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4c6c8-116">*pScalingRotation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c6c8-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6c8-117">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c6c8-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4c6c8-118">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui spécifie la rotation de la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="4c6c8-119">Si cet argument a la **valeur null**, une matrice Identity M <sub>SR</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4c6c8-120">*pScaling* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c6c8-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6c8-121">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c6c8-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4c6c8-122">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , le vecteur de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="4c6c8-123">Si cet argument a la **valeur null**, une matrice d’identité MS est appliquée à la formule dans les notes.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4c6c8-124">*pRotationCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c6c8-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6c8-125">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c6c8-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4c6c8-126">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , un point qui identifie le centre de rotation.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="4c6c8-127">Si cet argument a la **valeur null**, une matrice Identity M <sub>RC</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4c6c8-128">*protique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c6c8-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6c8-129">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c6c8-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4c6c8-130">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui spécifie la rotation.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="4c6c8-131">Si cet argument a la **valeur null**, une matrice Identity M <sub>r</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4c6c8-132">*pTranslation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c6c8-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6c8-133">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c6c8-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4c6c8-134">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) représentant la translation.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="4c6c8-135">Si cet argument a la **valeur null**, une matrice Identity MT est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c6c8-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c6c8-136">Return value</span></span>

<span data-ttu-id="4c6c8-137">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c6c8-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4c6c8-138">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c6c8-139">Notes</span><span class="sxs-lookup"><span data-stu-id="4c6c8-139">Remarks</span></span>

<span data-ttu-id="4c6c8-140">Cette fonction calcule la matrice de transformation avec la formule suivante, avec la concaténation de matrice évaluée dans l’ordre de gauche à droite :</span><span class="sxs-lookup"><span data-stu-id="4c6c8-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="4c6c8-141">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="4c6c8-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="4c6c8-142">où :</span><span class="sxs-lookup"><span data-stu-id="4c6c8-142">where:</span></span>

<span data-ttu-id="4c6c8-143">M <sub>out</sub> = matrice de sortie (*moue*)</span><span class="sxs-lookup"><span data-stu-id="4c6c8-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="4c6c8-144">M <sub>SC</sub> = matrice du centre de mise à l’échelle (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="4c6c8-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="4c6c8-145">M <sub>SR</sub> = matrice de rotation de la mise à l’échelle (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="4c6c8-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="4c6c8-146">MS = matrice de mise à l’échelle (*pScaling*)</span><span class="sxs-lookup"><span data-stu-id="4c6c8-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="4c6c8-147">M <sub>RC</sub> = Centre de rotation de la matrice (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="4c6c8-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="4c6c8-148">M <sub>r</sub> = matrice de rotation (*protique*)</span><span class="sxs-lookup"><span data-stu-id="4c6c8-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="4c6c8-149">MT = matrice de translation (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="4c6c8-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="4c6c8-150">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="4c6c8-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4c6c8-151">De cette façon, la fonction **D3DXMatrixTransformation** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4c6c8-152">Pour les transformations 2D, utilisez [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="4c6c8-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c6c8-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c6c8-153">Requirements</span></span>



| <span data-ttu-id="4c6c8-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c6c8-154">Requirement</span></span> | <span data-ttu-id="4c6c8-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c6c8-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c6c8-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c6c8-156">Header</span></span><br/>  | <dl> <span data-ttu-id="4c6c8-157"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c6c8-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4c6c8-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4c6c8-158">Library</span></span><br/> | <dl> <span data-ttu-id="4c6c8-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c6c8-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c6c8-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c6c8-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c6c8-161">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="4c6c8-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4c6c8-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="4c6c8-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="4c6c8-163">Transformations (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4c6c8-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




