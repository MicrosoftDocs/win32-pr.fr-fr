---
description: Crée une matrice de projection de perspective personnalisée de gauche.
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: D3DXMatrixPerspectiveOffCenterLH, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15743af16be84587fd8dc03e845ffcd8bd8dbc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529590"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="be337-103">D3DXMatrixPerspectiveOffCenterLH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="be337-103">D3DXMatrixPerspectiveOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="be337-104">Crée une matrice de projection de perspective personnalisée de gauche.</span><span class="sxs-lookup"><span data-stu-id="be337-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="be337-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be337-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="be337-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be337-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be337-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="be337-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be337-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="be337-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="be337-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="be337-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="be337-110">*l* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be337-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be337-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be337-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be337-112">Valeur x minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="be337-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="be337-113">*r* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be337-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be337-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be337-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be337-115">Valeur x maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="be337-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="be337-116">*b* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be337-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be337-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be337-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be337-118">Valeur y minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="be337-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="be337-119">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be337-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be337-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be337-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be337-121">Valeur y maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="be337-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="be337-122">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be337-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be337-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be337-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be337-124">Valeur z minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="be337-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="be337-125">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be337-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be337-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be337-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be337-127">Valeur z maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="be337-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be337-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be337-128">Return value</span></span>

<span data-ttu-id="be337-129">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="be337-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="be337-130">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de projection de perspective personnalisée de gauche.</span><span class="sxs-lookup"><span data-stu-id="be337-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="be337-131">Notes</span><span class="sxs-lookup"><span data-stu-id="be337-131">Remarks</span></span>

<span data-ttu-id="be337-132">Tous les paramètres de la fonction **D3DXMatrixPerspectiveOffCenterLH** sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="be337-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="be337-133">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="be337-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="be337-134">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="be337-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="be337-135">De cette façon, la fonction **D3DXMatrixPerspectiveOffCenterLH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="be337-135">In this way, the **D3DXMatrixPerspectiveOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="be337-136">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="be337-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="be337-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be337-137">Requirements</span></span>



| <span data-ttu-id="be337-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be337-138">Requirement</span></span> | <span data-ttu-id="be337-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="be337-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be337-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="be337-140">Header</span></span><br/>  | <dl> <span data-ttu-id="be337-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="be337-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="be337-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be337-142">Library</span></span><br/> | <dl> <span data-ttu-id="be337-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be337-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be337-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be337-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be337-145">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="be337-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="be337-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="be337-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="be337-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="be337-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="be337-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="be337-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="be337-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="be337-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="be337-150">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="be337-150">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
