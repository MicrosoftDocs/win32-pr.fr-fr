---
description: Génère une matrice de projection de perspective à gauche
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
ms.openlocfilehash: 400967b5e4a25244c50dbd6093fa2079700ba4eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543571"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx10mathh"></a><span data-ttu-id="b2fdd-103">D3DXMatrixPerspectiveLH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b2fdd-103">D3DXMatrixPerspectiveLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="b2fdd-104">Génère une matrice de projection de perspective à gauche</span><span class="sxs-lookup"><span data-stu-id="b2fdd-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="b2fdd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2fdd-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="b2fdd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2fdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2fdd-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b2fdd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fdd-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2fdd-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b2fdd-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b2fdd-110">*w* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2fdd-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fdd-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2fdd-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2fdd-112">Largeur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b2fdd-113">*h* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2fdd-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fdd-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2fdd-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2fdd-115">Hauteur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b2fdd-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2fdd-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fdd-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2fdd-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2fdd-118">Valeur Z du plan de vue proche.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b2fdd-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2fdd-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fdd-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2fdd-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2fdd-121">Valeur Z du plan d’affichage Far.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2fdd-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2fdd-122">Return value</span></span>

<span data-ttu-id="b2fdd-123">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2fdd-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b2fdd-124">Pointeur vers une structure D3DXMATRIX qui est une matrice de projection de perspective de gauche.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2fdd-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b2fdd-125">Remarks</span></span>

<span data-ttu-id="b2fdd-126">Tous les paramètres de la fonction D3DXMatrixPerspectiveLH sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-126">All the parameters of the D3DXMatrixPerspectiveLH function are distances in camera space.</span></span> <span data-ttu-id="b2fdd-127">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="b2fdd-128">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b2fdd-129">De cette façon, la fonction D3DXMatrixPerspectiveLH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-129">In this way, the D3DXMatrixPerspectiveLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b2fdd-130">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="b2fdd-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="b2fdd-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2fdd-131">Requirements</span></span>



| <span data-ttu-id="b2fdd-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2fdd-132">Requirement</span></span> | <span data-ttu-id="b2fdd-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2fdd-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2fdd-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2fdd-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b2fdd-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2fdd-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b2fdd-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b2fdd-136">Library</span></span><br/> | <dl> <span data-ttu-id="b2fdd-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2fdd-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2fdd-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2fdd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2fdd-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="b2fdd-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
