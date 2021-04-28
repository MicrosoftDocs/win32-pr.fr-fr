---
description: 'D3DXMatrixPerspectiveLH, fonction (D3dx9math. h) : génère une matrice de projection de perspective à gauche'
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
ms.openlocfilehash: d898a7d40cd1c9f7b46100c19d86573806ccb1b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118307"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx9mathh"></a><span data-ttu-id="02227-103">D3DXMatrixPerspectiveLH, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="02227-103">D3DXMatrixPerspectiveLH function (D3dx9math.h)</span></span>

<span data-ttu-id="02227-104">Génère une matrice de projection de perspective à gauche</span><span class="sxs-lookup"><span data-stu-id="02227-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="02227-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02227-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="02227-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02227-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02227-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="02227-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="02227-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="02227-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="02227-109">Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="02227-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="02227-110">*w* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02227-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02227-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02227-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02227-112">Largeur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="02227-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="02227-113">*h* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02227-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02227-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02227-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02227-115">Hauteur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="02227-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="02227-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02227-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02227-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02227-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02227-118">Valeur Z du plan de vue proche.</span><span class="sxs-lookup"><span data-stu-id="02227-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="02227-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02227-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02227-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02227-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02227-121">Valeur Z du plan d’affichage Far.</span><span class="sxs-lookup"><span data-stu-id="02227-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02227-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="02227-122">Return value</span></span>

<span data-ttu-id="02227-123">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="02227-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="02227-124">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) qui est une matrice de projection de perspective de gauche.</span><span class="sxs-lookup"><span data-stu-id="02227-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="02227-125">Notes </span><span class="sxs-lookup"><span data-stu-id="02227-125">Remarks</span></span>

<span data-ttu-id="02227-126">Tous les paramètres de la fonction **D3DXMatrixPerspectiveLH** sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="02227-126">All the parameters of the **D3DXMatrixPerspectiveLH** function are distances in camera space.</span></span> <span data-ttu-id="02227-127">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="02227-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="02227-128">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="02227-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="02227-129">De cette façon, la fonction **D3DXMatrixPerspectiveLH** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="02227-129">In this way, the **D3DXMatrixPerspectiveLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="02227-130">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="02227-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="02227-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02227-131">Requirements</span></span>



| <span data-ttu-id="02227-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02227-132">Requirement</span></span> | <span data-ttu-id="02227-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="02227-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02227-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="02227-134">Header</span></span><br/>  | <dl> <span data-ttu-id="02227-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="02227-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="02227-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="02227-136">Library</span></span><br/> | <dl> <span data-ttu-id="02227-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02227-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02227-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02227-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02227-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="02227-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="02227-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="02227-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="02227-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="02227-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="02227-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="02227-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="02227-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="02227-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="02227-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="02227-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
