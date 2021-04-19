---
description: Crée une matrice de projection de perspective pour un système droitier.
ms.assetid: 324c8a21-24ef-4b3a-aac1-a753e26076d4
title: D3DXMatrixPerspectiveRH, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eb1c2b4b876fb2dda842912d2f18f845a3167406
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539473"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx10mathh"></a><span data-ttu-id="312ec-103">D3DXMatrixPerspectiveRH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="312ec-103">D3DXMatrixPerspectiveRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="312ec-104">Crée une matrice de projection de perspective pour un système droitier.</span><span class="sxs-lookup"><span data-stu-id="312ec-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="312ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="312ec-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="312ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="312ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="312ec-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="312ec-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="312ec-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="312ec-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="312ec-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="312ec-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="312ec-110">*w* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="312ec-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="312ec-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="312ec-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="312ec-112">Largeur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="312ec-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="312ec-113">*h* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="312ec-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="312ec-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="312ec-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="312ec-115">Hauteur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="312ec-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="312ec-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="312ec-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="312ec-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="312ec-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="312ec-118">Valeur Z du plan de vue proche.</span><span class="sxs-lookup"><span data-stu-id="312ec-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="312ec-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="312ec-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="312ec-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="312ec-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="312ec-121">Valeur Z du plan d’affichage Far.</span><span class="sxs-lookup"><span data-stu-id="312ec-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="312ec-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="312ec-122">Return value</span></span>

<span data-ttu-id="312ec-123">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="312ec-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="312ec-124">Pointeur vers une structure D3DXMATRIX qui est une matrice de projection de perspective à droite.</span><span class="sxs-lookup"><span data-stu-id="312ec-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="312ec-125">Notes</span><span class="sxs-lookup"><span data-stu-id="312ec-125">Remarks</span></span>

<span data-ttu-id="312ec-126">Tous les paramètres de la fonction D3DXMatrixPerspectiveRH sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="312ec-126">All the parameters of the D3DXMatrixPerspectiveRH function are distances in camera space.</span></span> <span data-ttu-id="312ec-127">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="312ec-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="312ec-128">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="312ec-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="312ec-129">De cette façon, la fonction D3DXMatrixPerspectiveRH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="312ec-129">In this way, the D3DXMatrixPerspectiveRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="312ec-130">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="312ec-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="312ec-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="312ec-131">Requirements</span></span>



| <span data-ttu-id="312ec-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="312ec-132">Requirement</span></span> | <span data-ttu-id="312ec-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="312ec-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="312ec-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="312ec-134">Header</span></span><br/>  | <dl> <span data-ttu-id="312ec-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="312ec-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="312ec-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="312ec-136">Library</span></span><br/> | <dl> <span data-ttu-id="312ec-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="312ec-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="312ec-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="312ec-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="312ec-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="312ec-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
