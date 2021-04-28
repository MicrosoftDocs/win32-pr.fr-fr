---
description: 'D3DXMatrixPerspectiveRH, fonction (D3DX10Math. h) : génère une matrice de projection de perspective à droite.'
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
ms.openlocfilehash: 03ffd99d016023612daa3de96ae29275d71074a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109007"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx10mathh"></a><span data-ttu-id="d1c0e-103">D3DXMatrixPerspectiveRH, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d1c0e-103">D3DXMatrixPerspectiveRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="d1c0e-104">Crée une matrice de projection de perspective pour un système droitier.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c0e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1c0e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="d1c0e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1c0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c0e-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d1c0e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1c0e-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d1c0e-109">Pointeur vers la structure [**D3DXMATRIX**](d3d10-d3dxmatrix.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-110">*w* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1c0e-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1c0e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1c0e-112">Largeur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-113">*h* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1c0e-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1c0e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1c0e-115">Hauteur du volume de la vue dans le plan de vue rapprochée.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-116">*Zn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1c0e-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1c0e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1c0e-118">Valeur Z du plan de vue proche.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-119">*ZF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1c0e-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-120">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1c0e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1c0e-121">Valeur Z du plan d’affichage Far.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c0e-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d1c0e-122">Return value</span></span>

<span data-ttu-id="d1c0e-123">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1c0e-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d1c0e-124">Pointeur vers une structure D3DXMATRIX qui est une matrice de projection de perspective à droite.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1c0e-125">Notes </span><span class="sxs-lookup"><span data-stu-id="d1c0e-125">Remarks</span></span>

<span data-ttu-id="d1c0e-126">Tous les paramètres de la fonction D3DXMatrixPerspectiveRH sont des distances dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-126">All the parameters of the D3DXMatrixPerspectiveRH function are distances in camera space.</span></span> <span data-ttu-id="d1c0e-127">Les paramètres décrivent les dimensions du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="d1c0e-128">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre moue.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d1c0e-129">De cette façon, la fonction D3DXMatrixPerspectiveRH peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-129">In this way, the D3DXMatrixPerspectiveRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d1c0e-130">Cette fonction utilise la formule suivante pour calculer la matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="d1c0e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1c0e-131">Requirements</span></span>



| <span data-ttu-id="d1c0e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1c0e-132">Requirement</span></span> | <span data-ttu-id="d1c0e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1c0e-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c0e-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1c0e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="d1c0e-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1c0e-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d1c0e-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1c0e-136">Library</span></span><br/> | <dl> <span data-ttu-id="d1c0e-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1c0e-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1c0e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1c0e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c0e-139">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="d1c0e-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
