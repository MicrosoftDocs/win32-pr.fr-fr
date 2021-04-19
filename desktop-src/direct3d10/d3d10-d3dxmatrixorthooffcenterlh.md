---
description: Crée une matrice de projection orthographique personnalisée de gauche.
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: D3DXMatrixOrthoOffCenterLH, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4292f2996b4a19b71531094e5bf39bf7c213b972
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531561"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="8d872-103">D3DXMatrixOrthoOffCenterLH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8d872-103">D3DXMatrixOrthoOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="8d872-104">Crée une matrice de projection orthographique personnalisée de gauche.</span><span class="sxs-lookup"><span data-stu-id="8d872-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d872-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d872-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="8d872-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d872-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d872-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8d872-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d872-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d872-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8d872-109">Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="8d872-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d872-110">*l* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d872-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d872-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d872-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d872-112">Valeur x minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="8d872-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8d872-113">*r* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d872-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d872-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d872-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d872-115">Valeur x maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="8d872-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8d872-116">*b* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d872-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d872-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d872-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d872-118">Valeur y minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="8d872-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8d872-119">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d872-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d872-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d872-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d872-121">Valeur y maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="8d872-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8d872-122">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d872-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d872-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d872-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d872-124">Valeur z minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="8d872-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8d872-125">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d872-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d872-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d872-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d872-127">Valeur z maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="8d872-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d872-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d872-128">Return value</span></span>

<span data-ttu-id="8d872-129">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d872-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8d872-130">Pointeur vers le [**D3DXMATRIX**](d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="8d872-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8d872-131">Notes</span><span class="sxs-lookup"><span data-stu-id="8d872-131">Remarks</span></span>

<span data-ttu-id="8d872-132">Le [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) est un cas spécial de la fonction D3DXMatrixOrthoOffCenterLH.</span><span class="sxs-lookup"><span data-stu-id="8d872-132">The [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) is a special case of the D3DXMatrixOrthoOffCenterLH function.</span></span> <span data-ttu-id="8d872-133">Pour créer la même projection à l’aide de D3DXMatrixOrthoOffCenterLH, utilisez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d872-133">To create the same projection using D3DXMatrixOrthoOffCenterLH, use the following values:</span></span>

<span data-ttu-id="8d872-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="8d872-134">l = -w/2,</span></span>

<span data-ttu-id="8d872-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="8d872-135">r = w/2,</span></span>

<span data-ttu-id="8d872-136">b =-h/2 et</span><span class="sxs-lookup"><span data-stu-id="8d872-136">b = -h/2, and</span></span>

<span data-ttu-id="8d872-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="8d872-137">t = h/2.</span></span>

<span data-ttu-id="8d872-138">Tous les paramètres de la fonction D3DXMatrixOrthoOffCenterLH sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="8d872-138">All the parameters of the D3DXMatrixOrthoOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="8d872-139">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="8d872-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="8d872-140">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="8d872-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8d872-141">De cette façon, la fonction D3DXMatrixOrthoOffCenterLH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="8d872-141">In this way, the D3DXMatrixOrthoOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8d872-142">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="8d872-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="8d872-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d872-143">Requirements</span></span>



| <span data-ttu-id="8d872-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d872-144">Requirement</span></span> | <span data-ttu-id="8d872-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d872-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d872-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d872-146">Header</span></span><br/>  | <dl> <span data-ttu-id="8d872-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d872-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8d872-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8d872-148">Library</span></span><br/> | <dl> <span data-ttu-id="8d872-149"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d872-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8d872-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d872-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d872-151">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="8d872-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
