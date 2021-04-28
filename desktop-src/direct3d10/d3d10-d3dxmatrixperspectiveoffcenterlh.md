---
description: 'D3DXMatrixPerspectiveOffCenterLH, fonction (D3DX10Math. h) : crée une matrice de projection de perspective personnalisée de gauche.'
ms.assetid: 73616fcc-1799-4e65-92b9-2d8f500c326e
title: D3DXMatrixPerspectiveOffCenterLH, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1116e24b48c9090739511894d28031ca921ed6ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109047"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="d398b-103">D3DXMatrixPerspectiveOffCenterLH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d398b-103">D3DXMatrixPerspectiveOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="d398b-104">Crée une matrice de projection de perspective personnalisée de gauche.</span><span class="sxs-lookup"><span data-stu-id="d398b-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d398b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d398b-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d398b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d398b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d398b-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d398b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d398b-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d398b-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d398b-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d398b-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d398b-110">*l* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d398b-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d398b-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d398b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d398b-112">Valeur x minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d398b-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d398b-113">*r* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d398b-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d398b-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d398b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d398b-115">Valeur x maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d398b-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d398b-116">*b* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d398b-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d398b-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d398b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d398b-118">Valeur y minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d398b-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d398b-119">*t* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d398b-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d398b-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d398b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d398b-121">Valeur y maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d398b-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d398b-122">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d398b-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d398b-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d398b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d398b-124">Valeur z minimale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d398b-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d398b-125">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d398b-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d398b-126">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d398b-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d398b-127">Valeur z maximale du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d398b-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d398b-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d398b-128">Return value</span></span>

<span data-ttu-id="d398b-129">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d398b-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d398b-130">Pointeur vers une structure D3DXMATRIX qui est une matrice de projection de perspective personnalisée de gauche.</span><span class="sxs-lookup"><span data-stu-id="d398b-130">Pointer to a D3DXMATRIX structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d398b-131">Notes </span><span class="sxs-lookup"><span data-stu-id="d398b-131">Remarks</span></span>

<span data-ttu-id="d398b-132">Tous les paramètres de la fonction D3DXMatrixPerspectiveOffCenterLH sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="d398b-132">All the parameters of the D3DXMatrixPerspectiveOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="d398b-133">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d398b-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="d398b-134">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="d398b-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d398b-135">De cette façon, la fonction D3DXMatrixPerspectiveOffCenterLH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="d398b-135">In this way, the D3DXMatrixPerspectiveOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d398b-136">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="d398b-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="d398b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d398b-137">Requirements</span></span>



| <span data-ttu-id="d398b-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d398b-138">Requirement</span></span> | <span data-ttu-id="d398b-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d398b-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d398b-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="d398b-140">Header</span></span><br/>  | <dl> <span data-ttu-id="d398b-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d398b-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d398b-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d398b-142">Library</span></span><br/> | <dl> <span data-ttu-id="d398b-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d398b-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d398b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d398b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d398b-145">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d398b-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
