---
description: Crée une matrice de transformation affine 3D. Les arguments NULL sont traités comme des transformations d’identité.
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: D3DXMatrixAffineTransformation, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 025485f0015e6f2d85851c8f0919f5462b2bdc3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323153"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a><span data-ttu-id="eb413-104">D3DXMatrixAffineTransformation, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="eb413-104">D3DXMatrixAffineTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="eb413-105">Crée une matrice de transformation affine 3D.</span><span class="sxs-lookup"><span data-stu-id="eb413-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="eb413-106">Les arguments **null** sont traités comme des transformations d’identité.</span><span class="sxs-lookup"><span data-stu-id="eb413-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb413-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb413-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="eb413-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb413-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb413-109">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eb413-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb413-110">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb413-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eb413-111">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="eb413-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eb413-112">*Mise à l’échelle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb413-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb413-113">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb413-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb413-114">Facteur d’échelle.</span><span class="sxs-lookup"><span data-stu-id="eb413-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="eb413-115">*pRotationCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb413-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb413-116">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb413-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eb413-117">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , point identifiant le centre de rotation.</span><span class="sxs-lookup"><span data-stu-id="eb413-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="eb413-118">Si cet argument a la **valeur null**, une matrice Identity M <sub>RC</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="eb413-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="eb413-119">*protique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb413-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb413-120">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb413-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="eb413-121">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) qui spécifie la rotation.</span><span class="sxs-lookup"><span data-stu-id="eb413-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="eb413-122">Si cet argument a la **valeur null**, une matrice Identity M <sub>r</sub> est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="eb413-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="eb413-123">*pTranslation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb413-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb413-124">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb413-124">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eb413-125">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) représentant la traduction.</span><span class="sxs-lookup"><span data-stu-id="eb413-125">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure representing the translation.</span></span> <span data-ttu-id="eb413-126">Si cet argument a la **valeur null**, une matrice Identity MT est appliquée à la formule dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="eb413-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb413-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb413-127">Return value</span></span>

<span data-ttu-id="eb413-128">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb413-128">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eb413-129">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de transformation affine.</span><span class="sxs-lookup"><span data-stu-id="eb413-129">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb413-130">Notes</span><span class="sxs-lookup"><span data-stu-id="eb413-130">Remarks</span></span>

<span data-ttu-id="eb413-131">Cette fonction calcule la matrice de transformation affine avec la formule suivante, avec la concaténation de matrice évaluée dans l’ordre de gauche à droite :</span><span class="sxs-lookup"><span data-stu-id="eb413-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="eb413-132">M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="eb413-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="eb413-133">où :</span><span class="sxs-lookup"><span data-stu-id="eb413-133">where:</span></span>

<span data-ttu-id="eb413-134">M <sub>out</sub> = matrice de sortie (*moue*)</span><span class="sxs-lookup"><span data-stu-id="eb413-134">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="eb413-135">MS = matrice de mise à l’échelle (*mise à l’échelle*)</span><span class="sxs-lookup"><span data-stu-id="eb413-135">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="eb413-136">M <sub>RC</sub> = Centre de rotation de la matrice (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="eb413-136">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="eb413-137">M <sub>r</sub> = matrice de rotation (*protique*)</span><span class="sxs-lookup"><span data-stu-id="eb413-137">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="eb413-138">MT = matrice de translation (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="eb413-138">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="eb413-139">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="eb413-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="eb413-140">De cette façon, la fonction **D3DXMatrixAffineTransformation** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="eb413-140">In this way, the **D3DXMatrixAffineTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="eb413-141">Pour les transformations affines 2D, utilisez [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="eb413-141">For 2D affine transformations, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb413-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb413-142">Requirements</span></span>



| <span data-ttu-id="eb413-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb413-143">Requirement</span></span> | <span data-ttu-id="eb413-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb413-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb413-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb413-145">Header</span></span><br/>  | <dl> <span data-ttu-id="eb413-146"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb413-146"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="eb413-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb413-147">Library</span></span><br/> | <dl> <span data-ttu-id="eb413-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb413-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb413-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb413-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb413-150">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="eb413-150">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="eb413-151">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="eb413-151">**D3DXMatrixTransformation**</span></span>](d3dxmatrixtransformation.md)
</dt> <dt>

[<span data-ttu-id="eb413-152">Transformations (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="eb413-152">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
