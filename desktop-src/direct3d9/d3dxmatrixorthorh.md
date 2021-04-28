---
description: 'D3DXMatrixOrthoRH, fonction (D3dx9math. h) : génère une matrice de projection orthographique droitier.'
ms.assetid: 6b9b50d5-0307-4fc7-a28d-8f42d2a21bf0
title: D3DXMatrixOrthoRH, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d34a8379851d80ae8734c7f32cc0dc5977af2088
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107437"
---
# <a name="d3dxmatrixorthorh-function-d3dx9mathh"></a><span data-ttu-id="0d582-103">D3DXMatrixOrthoRH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0d582-103">D3DXMatrixOrthoRH function (D3dx9math.h)</span></span>

<span data-ttu-id="0d582-104">Génère une matrice de projection orthographique droitier.</span><span class="sxs-lookup"><span data-stu-id="0d582-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d582-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d582-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="0d582-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d582-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0d582-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d582-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d582-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0d582-109">Pointeur vers le [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="0d582-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d582-110">*w* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d582-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d582-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d582-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d582-112">Largeur du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="0d582-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0d582-113">*h* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d582-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d582-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d582-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d582-115">Hauteur du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="0d582-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0d582-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d582-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d582-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d582-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d582-118">Valeur z minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="0d582-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0d582-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d582-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d582-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d582-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d582-121">Valeur z maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="0d582-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d582-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d582-122">Return value</span></span>

<span data-ttu-id="0d582-123">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d582-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0d582-124">Pointeur vers le [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="0d582-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d582-125">Notes </span><span class="sxs-lookup"><span data-stu-id="0d582-125">Remarks</span></span>

<span data-ttu-id="0d582-126">Tous les paramètres de la fonction **D3DXMatrixOrthoRH** sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="0d582-126">All the parameters of the **D3DXMatrixOrthoRH** function are distances in camera space.</span></span> <span data-ttu-id="0d582-127">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="0d582-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="0d582-128">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="0d582-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0d582-129">De cette façon, la fonction **D3DXMatrixOrthoRH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="0d582-129">In this way, the **D3DXMatrixOrthoRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0d582-130">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="0d582-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="0d582-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d582-131">Requirements</span></span>



| <span data-ttu-id="0d582-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d582-132">Requirement</span></span> | <span data-ttu-id="0d582-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d582-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d582-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d582-134">Header</span></span><br/>  | <dl> <span data-ttu-id="0d582-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d582-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0d582-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d582-136">Library</span></span><br/> | <dl> <span data-ttu-id="0d582-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d582-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0d582-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d582-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d582-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="0d582-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0d582-140">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="0d582-140">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="0d582-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="0d582-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="0d582-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="0d582-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
