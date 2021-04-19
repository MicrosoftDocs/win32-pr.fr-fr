---
description: Génère une matrice de projection de perspective à gauche
ms.assetid: 07bbbca8-ad1e-4177-97d4-601b33179b47
title: D3DXMatrixPerspectiveLH, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf7e6a446202a86e126b2cea0c4a09f19bf6ffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522376"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx9mathh"></a><span data-ttu-id="fc72b-103">D3DXMatrixPerspectiveLH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fc72b-103">D3DXMatrixPerspectiveLH function (D3dx9math.h)</span></span>

<span data-ttu-id="fc72b-104">Génère une matrice de projection de perspective à gauche</span><span class="sxs-lookup"><span data-stu-id="fc72b-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="fc72b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc72b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="fc72b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc72b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc72b-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fc72b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc72b-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc72b-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fc72b-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="fc72b-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fc72b-110">*w* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc72b-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc72b-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc72b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc72b-112">Largeur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="fc72b-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="fc72b-113">*h* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc72b-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc72b-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc72b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc72b-115">Hauteur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="fc72b-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="fc72b-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc72b-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc72b-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc72b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc72b-118">Valeur Z du plan de vue proche.</span><span class="sxs-lookup"><span data-stu-id="fc72b-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="fc72b-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc72b-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc72b-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc72b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc72b-121">Valeur Z du plan d’affichage Far.</span><span class="sxs-lookup"><span data-stu-id="fc72b-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc72b-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc72b-122">Return value</span></span>

<span data-ttu-id="fc72b-123">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc72b-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fc72b-124">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de projection de perspective de gauche.</span><span class="sxs-lookup"><span data-stu-id="fc72b-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc72b-125">Notes</span><span class="sxs-lookup"><span data-stu-id="fc72b-125">Remarks</span></span>

<span data-ttu-id="fc72b-126">Tous les paramètres de la fonction **D3DXMatrixPerspectiveLH** sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="fc72b-126">All the parameters of the **D3DXMatrixPerspectiveLH** function are distances in camera space.</span></span> <span data-ttu-id="fc72b-127">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="fc72b-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="fc72b-128">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="fc72b-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fc72b-129">De cette façon, la fonction **D3DXMatrixPerspectiveLH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="fc72b-129">In this way, the **D3DXMatrixPerspectiveLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fc72b-130">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="fc72b-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="fc72b-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc72b-131">Requirements</span></span>



| <span data-ttu-id="fc72b-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc72b-132">Requirement</span></span> | <span data-ttu-id="fc72b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc72b-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc72b-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc72b-134">Header</span></span><br/>  | <dl> <span data-ttu-id="fc72b-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc72b-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fc72b-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc72b-136">Library</span></span><br/> | <dl> <span data-ttu-id="fc72b-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc72b-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc72b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc72b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc72b-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="fc72b-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fc72b-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="fc72b-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="fc72b-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="fc72b-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="fc72b-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="fc72b-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="fc72b-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="fc72b-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="fc72b-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="fc72b-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
