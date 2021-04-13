---
description: Génère une matrice de projection orthographique de gauche.
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: D3DXMatrixOrthoLH, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4aaf4a1a770ba0200a6afe389d37e248b9f4c7de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323146"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a><span data-ttu-id="c308a-103">D3DXMatrixOrthoLH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c308a-103">D3DXMatrixOrthoLH function (D3dx9math.h)</span></span>

<span data-ttu-id="c308a-104">Génère une matrice de projection orthographique de gauche.</span><span class="sxs-lookup"><span data-stu-id="c308a-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c308a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c308a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="c308a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c308a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c308a-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c308a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c308a-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c308a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c308a-109">Pointeur vers le [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="c308a-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="c308a-110">*w* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c308a-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c308a-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c308a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c308a-112">Largeur du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="c308a-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c308a-113">*h* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c308a-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c308a-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c308a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c308a-115">Hauteur du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="c308a-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c308a-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c308a-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c308a-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c308a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c308a-118">Valeur z minimale du volume de la vue, appelée z-near.</span><span class="sxs-lookup"><span data-stu-id="c308a-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="c308a-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c308a-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c308a-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c308a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c308a-121">Valeur z maximale du volume de la vue, appelée z-Far.</span><span class="sxs-lookup"><span data-stu-id="c308a-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c308a-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c308a-122">Return value</span></span>

<span data-ttu-id="c308a-123">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c308a-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c308a-124">Pointeur vers le [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="c308a-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c308a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c308a-125">Remarks</span></span>

<span data-ttu-id="c308a-126">Tous les paramètres de la fonction **D3DXMatrixOrthoLH** sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="c308a-126">All the parameters of the **D3DXMatrixOrthoLH** function are distances in camera space.</span></span> <span data-ttu-id="c308a-127">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="c308a-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="c308a-128">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="c308a-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c308a-129">De cette façon, la fonction **D3DXMatrixOrthoLH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="c308a-129">In this way, the **D3DXMatrixOrthoLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c308a-130">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="c308a-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a><span data-ttu-id="c308a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c308a-131">Requirements</span></span>



| <span data-ttu-id="c308a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c308a-132">Requirement</span></span> | <span data-ttu-id="c308a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c308a-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c308a-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c308a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c308a-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c308a-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c308a-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c308a-136">Library</span></span><br/> | <dl> <span data-ttu-id="c308a-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c308a-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c308a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c308a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c308a-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="c308a-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c308a-140">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="c308a-140">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="c308a-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="c308a-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="c308a-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="c308a-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
