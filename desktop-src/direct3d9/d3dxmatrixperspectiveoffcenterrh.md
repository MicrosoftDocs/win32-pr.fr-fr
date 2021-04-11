---
description: Crée une matrice de projection de perspective personnalisée et droitier.
ms.assetid: e6826e46-fc80-41fa-b0d8-45b6797df76f
title: D3DXMatrixPerspectiveOffCenterRH, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c4f211c6f57f60f8399fb5639edd07c3fc02377
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211882"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="6efc1-103">D3DXMatrixPerspectiveOffCenterRH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6efc1-103">D3DXMatrixPerspectiveOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="6efc1-104">Crée une matrice de projection de perspective personnalisée et droitier.</span><span class="sxs-lookup"><span data-stu-id="6efc1-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6efc1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6efc1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="6efc1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6efc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6efc1-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6efc1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efc1-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6efc1-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6efc1-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6efc1-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6efc1-110">*l* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6efc1-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6efc1-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efc1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6efc1-112">Valeur x minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="6efc1-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6efc1-113">*r* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6efc1-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6efc1-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efc1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6efc1-115">Valeur x maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="6efc1-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6efc1-116">*b* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6efc1-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6efc1-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efc1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6efc1-118">Valeur y minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="6efc1-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6efc1-119">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6efc1-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6efc1-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efc1-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6efc1-121">Valeur y maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="6efc1-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6efc1-122">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6efc1-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6efc1-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efc1-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6efc1-124">Valeur z minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="6efc1-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6efc1-125">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6efc1-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6efc1-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6efc1-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6efc1-127">Valeur z maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="6efc1-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6efc1-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6efc1-128">Return value</span></span>

<span data-ttu-id="6efc1-129">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6efc1-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6efc1-130">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de projection de perspective personnalisée et droitier.</span><span class="sxs-lookup"><span data-stu-id="6efc1-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="6efc1-131">Notes</span><span class="sxs-lookup"><span data-stu-id="6efc1-131">Remarks</span></span>

<span data-ttu-id="6efc1-132">Tous les paramètres de la fonction **D3DXMatrixPerspectiveOffCenterRH** sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="6efc1-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="6efc1-133">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="6efc1-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="6efc1-134">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="6efc1-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6efc1-135">De cette façon, la fonction **D3DXMatrixPerspectiveOffCenterRH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="6efc1-135">In this way, the **D3DXMatrixPerspectiveOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6efc1-136">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="6efc1-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="6efc1-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6efc1-137">Requirements</span></span>



| <span data-ttu-id="6efc1-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6efc1-138">Requirement</span></span> | <span data-ttu-id="6efc1-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="6efc1-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6efc1-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="6efc1-140">Header</span></span><br/>  | <dl> <span data-ttu-id="6efc1-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6efc1-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6efc1-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6efc1-142">Library</span></span><br/> | <dl> <span data-ttu-id="6efc1-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6efc1-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6efc1-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6efc1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6efc1-145">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="6efc1-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6efc1-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="6efc1-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="6efc1-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="6efc1-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="6efc1-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="6efc1-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="6efc1-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="6efc1-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="6efc1-150">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="6efc1-150">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
