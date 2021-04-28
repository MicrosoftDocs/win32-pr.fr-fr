---
description: 'D3DXMatrixPerspectiveLH, fonction (D3DX10Math. h) : génère une matrice de projection de perspective à gauche'
ms.assetid: 5fd8da67-ff12-42fa-b915-b50fa2680b32
title: D3DXMatrixPerspectiveLH, fonction (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0f6c976f64fe64d3ca583351ae5c7c32aa958fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109097"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx10mathh"></a><span data-ttu-id="b9e8e-103">D3DXMatrixPerspectiveLH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b9e8e-103">D3DXMatrixPerspectiveLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="b9e8e-104">Génère une matrice de projection de perspective à gauche</span><span class="sxs-lookup"><span data-stu-id="b9e8e-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e8e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9e8e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="b9e8e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9e8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e8e-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b9e8e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e8e-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9e8e-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b9e8e-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b9e8e-110">*w* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9e8e-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e8e-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9e8e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9e8e-112">Largeur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b9e8e-113">*h* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9e8e-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e8e-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9e8e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9e8e-115">Hauteur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b9e8e-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9e8e-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e8e-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9e8e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9e8e-118">Valeur Z du plan de vue proche.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b9e8e-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9e8e-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e8e-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9e8e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9e8e-121">Valeur Z du plan d’affichage Far.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9e8e-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b9e8e-122">Return value</span></span>

<span data-ttu-id="b9e8e-123">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9e8e-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b9e8e-124">Pointeur vers une structure D3DXMATRIX qui est une matrice de projection de perspective de gauche.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9e8e-125">Notes </span><span class="sxs-lookup"><span data-stu-id="b9e8e-125">Remarks</span></span>

<span data-ttu-id="b9e8e-126">Tous les paramètres de la fonction D3DXMatrixPerspectiveLH sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-126">All the parameters of the D3DXMatrixPerspectiveLH function are distances in camera space.</span></span> <span data-ttu-id="b9e8e-127">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="b9e8e-128">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b9e8e-129">De cette façon, la fonction D3DXMatrixPerspectiveLH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-129">In this way, the D3DXMatrixPerspectiveLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b9e8e-130">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="b9e8e-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="b9e8e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9e8e-131">Requirements</span></span>



| <span data-ttu-id="b9e8e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9e8e-132">Requirement</span></span> | <span data-ttu-id="b9e8e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9e8e-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e8e-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9e8e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b9e8e-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e8e-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b9e8e-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b9e8e-136">Library</span></span><br/> | <dl> <span data-ttu-id="b9e8e-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9e8e-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9e8e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9e8e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e8e-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b9e8e-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
