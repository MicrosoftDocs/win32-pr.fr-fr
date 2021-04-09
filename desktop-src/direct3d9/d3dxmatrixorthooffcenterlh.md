---
description: Crée une matrice de projection orthographique personnalisée de gauche.
ms.assetid: e4f087e5-63d9-49ca-9d8e-3a25070e1a51
title: D3DXMatrixOrthoOffCenterLH, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e286197233b2abb2b19138b8fc9d154df355a6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953942"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="20ffa-103">D3DXMatrixOrthoOffCenterLH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="20ffa-103">D3DXMatrixOrthoOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="20ffa-104">Crée une matrice de projection orthographique personnalisée de gauche.</span><span class="sxs-lookup"><span data-stu-id="20ffa-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ffa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20ffa-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="20ffa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20ffa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20ffa-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="20ffa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="20ffa-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="20ffa-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="20ffa-109">Pointeur vers le [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="20ffa-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ffa-110">*l* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20ffa-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ffa-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20ffa-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20ffa-112">Valeur x minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="20ffa-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="20ffa-113">*r* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20ffa-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ffa-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20ffa-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20ffa-115">Valeur x maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="20ffa-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="20ffa-116">*b* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20ffa-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ffa-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20ffa-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20ffa-118">Valeur y minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="20ffa-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="20ffa-119">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20ffa-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ffa-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20ffa-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20ffa-121">Valeur y maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="20ffa-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="20ffa-122">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20ffa-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ffa-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20ffa-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20ffa-124">Valeur z minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="20ffa-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="20ffa-125">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20ffa-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ffa-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20ffa-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20ffa-127">Valeur z maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="20ffa-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20ffa-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20ffa-128">Return value</span></span>

<span data-ttu-id="20ffa-129">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="20ffa-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="20ffa-130">Pointeur vers le [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="20ffa-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="20ffa-131">Notes</span><span class="sxs-lookup"><span data-stu-id="20ffa-131">Remarks</span></span>

<span data-ttu-id="20ffa-132">La fonction [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) est un cas particulier de la fonction **D3DXMatrixOrthoOffCenterLH** .</span><span class="sxs-lookup"><span data-stu-id="20ffa-132">The [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) function is a special case of the **D3DXMatrixOrthoOffCenterLH** function.</span></span> <span data-ttu-id="20ffa-133">Pour créer la même projection à l’aide de **D3DXMatrixOrthoOffCenterLH**, utilisez les valeurs suivantes : l =-w/2, r = w/2, b =-h/2 et t = h/2.</span><span class="sxs-lookup"><span data-stu-id="20ffa-133">To create the same projection using **D3DXMatrixOrthoOffCenterLH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="20ffa-134">Tous les paramètres de la fonction **D3DXMatrixOrthoOffCenterLH** sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="20ffa-134">All the parameters of the **D3DXMatrixOrthoOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="20ffa-135">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="20ffa-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="20ffa-136">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="20ffa-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="20ffa-137">De cette façon, la fonction **D3DXMatrixOrthoOffCenterLH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="20ffa-137">In this way, the **D3DXMatrixOrthoOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="20ffa-138">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="20ffa-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="20ffa-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20ffa-139">Requirements</span></span>



| <span data-ttu-id="20ffa-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20ffa-140">Requirement</span></span> | <span data-ttu-id="20ffa-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="20ffa-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffa-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="20ffa-142">Header</span></span><br/>  | <dl> <span data-ttu-id="20ffa-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="20ffa-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="20ffa-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20ffa-144">Library</span></span><br/> | <dl> <span data-ttu-id="20ffa-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20ffa-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="20ffa-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20ffa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ffa-147">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="20ffa-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="20ffa-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="20ffa-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="20ffa-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="20ffa-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="20ffa-150">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="20ffa-150">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> </dl>

 

 
